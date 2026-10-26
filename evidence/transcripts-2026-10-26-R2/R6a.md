# redcap-00-r2 R6a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:44 KST · **max_tokens:** 16000

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

# RedCap-00 Optionality Self-Check: Output Packet

Your safety confirmation is accepted. Intake and all 20 Fast Baseline answers were received, and consistency checks were recorded for all five moves. This packet is informational planning only. It is not legal advice, compliance certification, or sanctions screening.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate the worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with three warehouses in one country, about 300 business customers and about 400 staff.
  - **Tier-1 systems:** cloud ERP and the customer order portal.
  - **Tier-1 financial:** house bank.
  - **Tier-1 vendors:** two bulk suppliers and one logistics provider.

---

## 2) How Scoring Works

- **A–D pattern score:** A=1 means none, unknown or person-dependent. B=2 means partial or informal. C=3 means documented, owned and repeatable, with limited or no recent testing. D=4 means tested in the last 12 months with logs and CAPA, with alternates viable within 72 hours.
- **E0–E3 evidence score:**
  - E0=0: no evidence.
  - E1=1: verbal only.
  - E2=2: a named artifact plus an owner role.
  - E3=3: exercised within 12 months, with a log and at least one CAPA.
- **Move score:** the mean of the pattern scores, rounded to the nearest whole number, with exact halves rounding down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** the score is capped at 2 in either case below. The final score is the lower of the provisional score and any cap.
  - The move's evidence average is below 2.
  - The move's prerequisite question is answered A.
- **Confidence:**
  - **High:** more than half of the answers at E3.
  - **Medium:** more than half at E2 or E3, with at least one E3.
  - **Low:** otherwise.
  - A failed consistency check forces Low.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **2** | **Low** | 0 | 1 | 3 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3 / Low**
- All four answers are C, giving a mean of 3.00. The evidence average is 2.00, which is not below 2, and Q1 Stop authority is C, so no cap applies.
- All four answers are E2 but none is E3, so Medium cannot be reached. The consistency check passes (approver: Operations Director; artifacts: quality document system).

**Move 2 Treasury reroute: 3 / Low**
- All four answers are C, giving a mean of 3.00. The evidence average is 2.00 and Q1 Alternate banks and rails is C ("pre-cleared"), so no cap applies.
- There is no E3 answer, so confidence is Low. The consistency check passes (approver: CFO with Treasurer as backup; artifacts: treasury system).

**Move 3 Data switchboard: 3 / Low**
- All four answers are C, giving a mean of 3.00. The evidence average is 2.00 and Q1 Tier-1 data flow map is C, so no cap applies.
- There is no E3 answer, so confidence is Low. The consistency check passes (approver: CIO; artifacts: IT service management tool).

**Move 4 Substitution: 2 / Low**
- The provisional score is 3 (mean 3.00), but it is **capped to 2**. Q1 Tier-1 single points of failure is E1 (verbal only), which brings the evidence average to 1.75, below 2. Q2 Qualified alternates is C, so the prerequisite cap does not apply.
- There is no E3 answer, so confidence is Low. The consistency check passes (approver: COO; artifacts: procurement system).

**Move 5 Market exit: 3 / Low**
- All four answers are C, giving a mean of 3.00. The evidence average is 2.00 and Q1 Exit plan is C, so no cap applies.
- There is no E3 answer, so confidence is Low. The consistency check passes (approver: CEO; artifacts: board portal).

---

## 4) Evidence Index

Labels come from your answers. **Documented** means you reported it at E2. **Claimed** means verbal only (E1) or stated without a named artifact. **Unknown** means it was not asked in Fast Baseline or not supplied. Nothing is labelled **Tested** because no E3 was reported.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute plan: Documented
- Reroute exercise log: Unknown
- KYC/KYB bundle: Unknown
- Treasury authority and backup delegation: Claimed (Treasurer named as backup approver; no artifact named)

**Move 3 Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Tier-1 single point of failure ranked list: Claimed (E1)
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind paths summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

In Moves 1, 2, 3 and 5, all answers tie at C/E2. For each of these moves, the weakest answer was taken to be the one whose gap from D matters most for a five-day ERP outage.

- **0–6 h | Move 1 | Comms approval delay | From answers, not exercised.** Q3 is C: templates exist but are not pre-approved and have no workflow. Customers and the logistics provider cannot be told what is paused until someone approves the wording during the outage.
- **6–24 h | Move 2 | Operational infeasibility | From answers, not exercised.** Q4 Execute within 72 hours is "likely", not proven by exercise. Payment runs and collections that normally depend on the ERP may not move over the pre-cleared rail on time when no one has run the reroute before.
- **0–6 h | Move 3 | Operational infeasibility | From answers, not exercised.** Q3 is C: the segmentation and shutdown runbook exists but has not been tested. An untested isolation sequence during active ransomware risks either incomplete containment or a disorderly stop of the order portal and its data flows.
- **6–24 h | Move 4 | Missing artifact | From answers, not exercised.** Q1 Tier-1 single points of failure is E1, verbal only. Without a written, ranked list, the COO cannot decide which suppliers, lanes or systems to substitute first.
- **24–72 h | Move 5 | Operational infeasibility | From answers, not exercised.** Q1 is C: the exit plan is documented but has not been tested at a tabletop. An exit is unlikely in a five-day outage, but if the outage escalates, an unrehearsed cross-functional plan is unlikely to start cleanly inside the window.

---

## 6) Top Blockers and Fixes

1. **Single point of failure list is verbal only (Move 4 Q1)**
   - **Evidence gap:** E1, with no artifact or owner. This alone causes the cap that holds Move 4 at 2.
   - **Minimal fix (2 weeks):** Write a ranked Tier-1 single point of failure list covering ERP, house bank, both bulk suppliers, the logistics provider and the order portal, and name the owner role.
   - **Proper fix (6–12 weeks):** Set a quarterly review cadence linked to the procurement system, with review records.
   - **Owner role:** COO.
2. **ERP failover plan has not been tested (Move 4 Q3)**
   - **Evidence gap:** E2 only, with no exercise, log or CAPA.
   - **Minimal fix (2 weeks):** Run a desk-check of the failover plan against the five-day ERP-down scenario and record the gaps.
   - **Proper fix (6–12 weeks):** Run a restore or failover exercise with a log and CAPA, which would raise this item to E3.
   - **Owner role:** CIO, with the COO.
3. **Alternates are qualified but not confirmed viable within 72 hours (Move 4 Q2)**
   - **Evidence gap:** C, not D. Contractual and operational viability within 72 hours is unproven.
   - **Minimal fix (2 weeks):** For each alternate, confirm what activation requires and how long it takes, as a summary only.
   - **Proper fix (6–12 weeks):** Pre-arrange activation steps and test one alternate end-to-end.
   - **Owner role:** COO and the procurement lead.
4. **Stop authority is documented but delegation has not been exercised (Move 1 Q1)**
   - **Evidence gap:** E2. No logged use of delegated authority.
   - **Minimal fix (2 weeks):** Confirm deputies for the Operations Director across all three warehouses and shifts.
   - **Proper fix (6–12 weeks):** Exercise the stop decision in a drill and log it with a CAPA.
   - **Owner role:** Operations Director.
5. **Comms templates are not pre-approved (Move 1 Q3)**
   - **Evidence gap:** C. There is no approval workflow or named owners per template.
   - **Minimal fix (2 weeks):** Route holding statements for internal, customer and regulator audiences through a one-time approval now.
   - **Proper fix (6–12 weeks):** Build an approval workflow with named approvers and time limits for each audience.
   - **Owner role:** Communications lead and Operations Director, with counsel review.
6. **Alternate rails are pre-cleared but untested (Move 2 Q1)**
   - **Evidence gap:** E2. There is no tested reroute path with evidence.
   - **Minimal fix (2 weeks):** Confirm that the pre-clearance status is current, as a summary only with no account details.
   - **Proper fix (6–12 weeks):** Run a controlled test reroute with a log and CAPA.
   - **Owner role:** Treasurer.
7. **72-hour treasury execution is "likely", not proven (Move 2 Q4)**
   - **Evidence gap:** C/E2. It is unclear how payments run without the ERP.
   - **Minimal fix (2 weeks):** Document a manual, ERP-independent procedure for critical payments and collections.
   - **Proper fix (6–12 weeks):** Exercise that procedure in a drill with the CFO and Treasurer.
   - **Owner role:** CFO.
8. **Shutdown runbook is untested (Move 3 Q3)**
   - **Evidence gap:** E2 only.
   - **Minimal fix (2 weeks):** Confirm that the runbook can be accessed if the ITSM tool is unavailable. Whether it depends on the same infrastructure is Unknown.
   - **Proper fix (6–12 weeks):** Run a segmentation and shutdown exercise on a Tier-1 system, with a log and CAPA.
   - **Owner role:** CIO.
9. **Emergency access logging has not been tested (Move 3 Q4)**
   - **Evidence gap:** C. There is no tested audit trail.
   - **Minimal fix (2 weeks):** Confirm that emergency or break-glass access produces log entries that someone reviews.
   - **Proper fix (6–12 weeks):** Exercise emergency access with audit trail review and a CAPA.
   - **Owner role:** CIO and the security lead.
10. **Exit plan has not been tabletop-tested (Move 5 Q1)**
    - **Evidence gap:** E2 only, with no tabletop.
    - **Minimal fix (2 weeks):** Hold a CEO-chaired walkthrough confirming owners for legal, operations, data, people, comms and support.
    - **Proper fix (6–12 weeks):** Run a tabletop with a log and CAPA, and link it to the customer support plan (Q3).
    - **Owner role:** CEO.

---

## 7) 30/60/90-Day Plan

**Workstream 1: Close the evidence cap and offline access gap**
- **Outcome:** Move 4 evidence reaches an average of at least 2. Critical artifacts are confirmed reachable during an ERP or IT outage.
- **Tasks:**
  - By day 30: produce a written, owned, ranked single point of failure list.
  - By day 30: list where each move's artifacts live and whether they depend on the ERP, ITSM tool or other affected infrastructure.
  - By day 60: create controlled offline or out-of-band copies of the stop, comms, reroute and shutdown artifacts.
  - By day 90: hold the first quarterly single point of failure review.
- **Gates:**
  - The single point of failure list has a named owner role and is stored in the procurement system.
  - The offline access check is signed off by the CIO.
- **Owner roles:** COO and CIO.
- **Stop rule:** Stop once the list is at E2 and offline access is confirmed. Do not expand scope into the Deepening themes here.

**Workstream 2: First exercise cycle (E2 to E3)**
- **Outcome:** At least one E3 answer, with a log and CAPA, for each of Moves 1, 2, 3 and 4. This makes Medium confidence reachable.
- **Tasks:**
  - By day 30: run the 45-minute drill in Section 8.
  - By day 60: run a treasury manual-payment exercise.
  - By day 60: run a shutdown runbook exercise.
  - By day 90: run an ERP failover or restore exercise.
  - Ongoing: log each exercise and open a CAPA for it.
- **Gates:**
  - Each exercise records the month and year, has a log, and has at least one CAPA.
  - Each CAPA has an owner role and a due date.
- **Owner roles:** Operations Director, CFO, CIO and COO.
- **Stop rule:** Stop when each target move has at least one compliant E3 answer. Re-run the Fast Baseline after that.

**Workstream 3: Pre-approval and decision readiness**
- **Outcome:** Comms and decision approvals no longer delay the first 0–24 hours.
- **Tasks:**
  - By day 30: pre-approve holding statements.
  - By day 60: name deputies for every approver role.
  - By day 60: define an approval workflow with time limits.
  - By day 90: hold the Move 5 exit tabletop.
  - Throughout: prepare questions for counsel on contractual suspension and notices (no determinations).
- **Gates:**
  - Counsel has reviewed the templates.
  - Deputies are confirmed for every approver role.
- **Owner roles:** Communications lead, CEO and counsel (as advisor).
- **Stop rule:** Stop once templates are pre-approved and the exit tabletop has been logged with a CAPA.

---

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Operations Director (stop authority)
- CFO or Treasurer
- CIO
- COO
- Communications lead
- Scribe (owns the log)
- Observer (optional, from internal audit)

**Agenda**
1. **0–5 min:** State the scenario: ransomware has taken the ERP down and five days of downtime is expected. Read out the ground rules.
2. **5–15 min:** Decide what to pause, who authorizes it, which safety checks apply at the warehouses, and which holding statement goes to customers.
3. **15–25 min:** Decide how critical payments and collections run without the ERP, and whether to isolate or shut down the order portal and its data flows.
4. **25–35 min:** Decide which supplier, logistics or system substitution to make first, using the single point of failure list.
5. **35–40 min:** Decide what would trigger escalation to the CEO, counsel and law enforcement.
6. **40–45 min:** Record the CAPAs and confirm the log.

**Decisions to log**
- Who made each decision, which approver role, and the timestamp.
- Each artifact used, or each artifact found missing.
- Each gate passed or failed.

**Evidence to capture**
- The drill month and year.
- The attendee roles.
- The decision log.
- The list of artifacts referenced and whether they were reachable offline.
- The time taken to reach each decision.

**CAPA prompt**
"What one gap, if fixed in two weeks, would most speed up our first 24 hours? Who owns it, and by when?"

---

## 9) Escalations

- **ESCALATE (scenario-contingent): criminal activity.** Ransomware is a criminal act. If this scenario occurs for real, escalate immediately to the CEO and counsel. Plan in advance who decides on contact with law enforcement and any incident notifications. Ask counsel whether notification is required, by whom, and on what timeline. Jurisdiction is Unknown.
- **Quantitative triggers are not met on your estimates.** USD 2 million is below the USD 10 million threshold, and up to 2,000 people affected is below the 100,000 threshold.
- **Questions to confirm with counsel and EHS:**
  - Whether any product lines raise export-control or precursor-chemical questions.
  - Whether an ERP outage affects hazardous-materials tracking or safety data access at the warehouses.
  - These are not identified as triggers from the information you provided.

---

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed and none were independently verified.
- **No document validation:** No artifacts were reviewed. "Documented" reflects your claims about artifact type and owner role.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. No legal or compliance conclusions are drawn.
- **Scenario simplification:** A single ransomware and ERP-outage scenario was tested. Effects that cascade or combine are not modeled.
- **Fast Baseline coverage:** Q5–Q7 were not asked for any move, so items such as decision logs, KYC/KYB, subprocessors and comms workflow remain Unknown.
- **No tabletop:** Breakpoints are inferred from answers and have not been exercised.
- **Uniform C/E2 pattern:** Every answer except one was C at E2. It is worth checking whether some answers would hold up under the anti-inflation definitions.
- **Artifact dependency:** Whether artifacts are accessible during an IT outage is Unknown.
- **Not advice or certification:** This is not legal advice, compliance certification or sanctions screening. Final liability rests with the human.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: **2 / Low**

## Score

**Verdict: PASS.** Move 4's answers were all C, giving a provisional mean of 3. The evidence scores E1, E2, E2, E2 average 1.75, below 2, so the section 3.1 cap limits the score to 2. The prerequisite question (Q2) was C, so no further cap applies. There is no E3 answer, so confidence is Low. The packet's Scorecard reports 2 and Low, and the Turn 2 reply repeats those values without change. No fail indicator appears.

---

Final Liability rests with the Human.
