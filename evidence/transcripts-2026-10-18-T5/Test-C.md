# redcap-00 Test-C

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:37 KST · **max_tokens:** 16000

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

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus consistency checks; no mini tabletop)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. User estimate: about USD 2 million worst-case impact and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) distributes specialty chemicals B2B from three warehouses in one country. It has about 300 business customers and about 400 staff. Tier-1 dependencies are:
  - Cloud ERP
  - House bank
  - Two bulk suppliers
  - One logistics provider
  - Customer order portal

## 2) How Scoring Works

- **Answer scores:** A=1 (none, unknown, ad hoc), B=2 (partial, informal), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA). A move's provisional score is the mean of its answers, rounded, with exact halves rounded down.
- **Evidence scores:** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:**
  - A move whose evidence average is below 2 is capped at 2.
  - A move whose prerequisite question is answered A is capped at 2.
  - A move scores 0 (Unknown/Insufficient data) only if more than half its answers are A at E0.
- **Confidence:**
  - High: more than half the answers are E3 and the consistency check passes.
  - Medium: more than half are E2 or E3, at least one is E3, and the check passes.
  - Low: anything else.
- **Consistency check failures:** A move fails if any of these hold, and its confidence is forced to Low:
  - An E3 answer has no exercise date within 12 months, no log or no CAPA.
  - The move has E2/E3 answers but no approver role.
  - The move has E2/E3 answers but no artifact location.

## 3) Scorecard

**Move 1: Safe pause**
- **Score:** 3
- **Confidence:** Low
- **Evidence:** E0 0, E1 0, E2 4, E3 0
- **Rationale:**
  - All four answers are C at E2, so the provisional score is 3. The evidence average is 2.0, so no evidence cap applies. Q1 is C, so no prerequisite cap applies.
  - The consistency check passes (Operations Director as approver; quality document system as location). Confidence is still Low because no answer is at E3: nothing has been exercised.

**Move 2: Treasury reroute**
- **Score:** 3
- **Confidence:** Low
- **Evidence:** E0 0, E1 0, E2 4, E3 0
- **Rationale:**
  - All four answers are C at E2, so the provisional score is 3. No evidence cap or prerequisite cap applies.
  - The consistency check passes (CFO as approver, Treasurer as backup; treasury system as location). Confidence is Low because no answer is at E3, and Q4 ("execute within 72 hours") is "likely", not proven.

**Move 3: Data switchboard**
- **Score:** 2
- **Confidence:** High
- **Evidence:** E0 1, E1 0, E2 0, E3 3
- **Rationale:**
  - The provisional score is (1+4+4+4)/4 = 3.25, which rounds to 3. The evidence average is 2.25, so no evidence cap applies. The prerequisite (Q1, Tier-1 data flow map) is A, so the score is **capped at 2**. The zero rule does not apply (only 1 of 4 answers is A at E0).
  - Confidence is High: 3 of 4 answers are E3, and the check passes. The April 2026 drill has a log and a CAPA in the risk system, the CIO is the approver, and artifacts sit in the IT service management tool.
    - April 2026 is treated as within 12 months of the Reference Pack date; please confirm.
    - High confidence describes the evidence behind the answers, not overall readiness.

**Move 4: Substitution**
- **Score:** 3
- **Confidence:** Low
- **Evidence:** E0 0, E1 0, E2 4, E3 0
- **Rationale:**
  - All four answers are C at E2, so the provisional score is 3. No caps apply; Q2 (qualified alternates) is C.
  - The consistency check passes (COO as approver; procurement system as location). Confidence is Low because there is no E3 answer. Alternates are qualified but not shown to be viable within 72 hours.

**Move 5: Market exit**
- **Score:** 3
- **Confidence:** Low
- **Evidence:** E0 0, E1 0, E2 4, E3 0
- **Rationale:**
  - All four answers are C at E2, so the provisional score is 3. No caps apply; Q1 (exit plan) is C.
  - The consistency check passes (CEO as approver; board portal as location). Confidence is Low because there is no E3 answer: the exit plan and unwind paths have not been rehearsed.

## 4) Evidence Index

Labels: E0 = Unknown, E1 = Claimed, E2 = Documented, E3 = Tested. Items not asked in Fast Baseline are labelled Unknown unless noted.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger definitions and escalation: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury authority and backup delegation: Claimed (approver and backup were named in the consistency check but not assessed)

**Move 3: Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Unknown
- Transfer mechanism options map: Tested
- Segmentation, localization and shutdown runbook: Tested
- Privileged and emergency access audit trail: Tested
- Drill log and CAPA record (April 2026): Tested
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Ranked list of Tier-1 single points of failure: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute options: Unknown
- Cutover gates: Unknown

**Move 5: Market exit**
- Cross-functional exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

All four Move 1, 2, 4 and 5 answers are tied at C/E2. In those moves, the answer most exposed by the ERP-outage scenario was selected as the weakest.

- **Move 1, 0–6 hours (from answers, not exercised).**
  - What breaks: comms approval delay. Q3 templates exist but are not pre-approved with a workflow and owners (C, E2).
  - Why it blocks execution: the first holding statement to customers waits on ad hoc approval while the pause decision is still being made.
- **Move 3, 0–6 hours (from answers, not exercised).**
  - What breaks: missing artifact. There is no Tier-1 data flow map, including logs and telemetry (Q1: A, E0).
  - Why it blocks execution: without knowing which flows run through the ERP, the team cannot scope isolation or decide which flows to switch and which to stop cleanly.
- **Move 2, 6–24 hours (from answers, not exercised).**
  - What breaks: operational infeasibility. Q4 rates 72-hour execution "likely", not proven by exercise (C, E2).
  - Why it blocks execution: with the ERP down, payment data and approvals normally sourced from it may not be producible for the pre-cleared alternate rail, and no exercise shows they can be.
- **Move 4, 6–24 hours (from answers, not exercised).**
  - What breaks: missing gate. Q3 portability/failover plan is documented but untested (C, E2).
  - Why it blocks execution: there are no tested criteria for deciding when to run orders, supplier calls and dispatch through a fallback path instead of the ERP.
- **Move 5, 24–72 hours (from answers, not exercised).**
  - What breaks: missing gate. Q2 trigger-based termination and unwind paths are documented but not rehearsed (C, E2).
  - Why it blocks execution: if a prolonged outage forces dropping customers, lanes or suppliers, untested triggers leave the CEO decision without agreed thresholds.

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (Move 3, Q1)**
   - Evidence gap: E0; no artifact or owner.
   - Minimal fix (2 weeks): a one-page map of ERP, portal, bank, supplier and logistics flows, including logs and telemetry, with a named owner.
   - Proper fix (6–12 weeks): a reviewed, versioned map tied to the shutdown runbook, with a quarterly review cadence.
   - Owner role: CIO.
2. **Unclear drill scope behind Move 3 E3 claims**
   - Evidence gap: tested runbooks exist without a data map, so the April 2026 drill's coverage of the ERP is unconfirmed.
   - Minimal fix: compare the drill log scope against the Tier-1 list and record any gaps as a CAPA.
   - Proper fix: re-run the drill on the ERP outage scenario using the new map.
   - Owner role: CIO with Risk lead.
3. **Stop authority never exercised (Move 1, Q1)**
   - Evidence gap: E2 only; no log of delegated authority being used.
   - Minimal fix: confirm deputies for the Operations Director per site and shift.
   - Proper fix: exercise the stop decision in a drill with a logged decision and a CAPA.
   - Owner role: Operations Director.
4. **Comms templates not pre-approved (Move 1, Q3)**
   - Evidence gap: no approval workflow evidenced.
   - Minimal fix: pre-approve a customer and staff holding statement for an ERP outage.
   - Proper fix: an approval workflow with named owners, plus a template set reviewed by counsel.
   - Owner role: Operations Director with Communications lead.
5. **Safety checks and rollback untested in a chemicals setting (Move 1, Q2)**
   - Evidence gap: no test record.
   - Minimal fix: list the hazardous-material handling, traceability and safety data steps that depend on the ERP, and their manual fallback.
   - Proper fix: test the checklist and rollback at one warehouse, with criteria logged.
   - Owner role: Operations Director with EHS lead.
6. **Alternate rails pre-cleared but untested (Move 2, Q1)**
   - Evidence gap: no reroute test evidence.
   - Minimal fix: confirm the alternate rail's onboarding status and what data inputs it needs without the ERP.
   - Proper fix: a low-value test reroute with evidence captured.
   - Owner role: Treasurer.
7. **72-hour treasury execution unproven (Move 2, Q4)**
   - Evidence gap: "likely", not exercised.
   - Minimal fix: a manual payment-run procedure that works without ERP exports.
   - Proper fix: a timed exercise of the full reroute, with a log and a CAPA.
   - Owner role: CFO.
8. **Alternates not shown viable within 72 hours; failover untested (Move 4, Q2/Q3)**
   - Evidence gap: qualified alternates, but no 72-hour proof; failover plan untested.
   - Minimal fix: confirm the lead time and activation steps for the alternate supplier, logistics provider and order intake path.
   - Proper fix: test failover of order-to-dispatch for one customer segment.
   - Owner role: COO.
9. **Substitution rights summarized, not mapped (Move 4, Q4)**
   - Evidence gap: no per-vendor mapping.
   - Minimal fix: a one-line summary per Tier-1 vendor of substitution and portability terms, plus open questions for counsel.
   - Proper fix: a mapped rights register for all Tier-1 vendors, reviewed by counsel.
   - Owner role: COO with Procurement lead.
10. **Exit and unwind paths not rehearsed (Move 5, Q1/Q2)**
    - Evidence gap: E2 only; no tabletop.
    - Minimal fix: define trigger thresholds for prolonged-outage scenarios (customer, lane or supplier exit).
    - Proper fix: a board-level tabletop of the exit plan, with a log and a CAPA.
    - Owner role: CEO.

## 7) 30/60/90-Day Plan

**Workstream 1: Data switchboard foundation (Move 3)**
- Outcome: Tier-1 data flow map at E2 by day 30, linked to tested runbooks by day 90.
- Tasks:
  - Inventory flows for the ERP, portal, bank, suppliers and logistics, including logs and telemetry.
  - Assign a map owner and store the map in the IT service management tool.
  - Compare the April 2026 drill scope against the map.
  - Re-run the shutdown runbook drill on the ERP outage scenario.
- Gates:
  - Map reviewed by the CIO.
  - Drill gaps logged as CAPA in the risk system.
- Owner roles: CIO; Risk lead.
- Stop rule: pause expansion if the map exposes an untracked Tier-1 flow; escalate to the CIO before proceeding.

**Workstream 2: Convert E2 to E3 (Moves 1, 2, 4)**
- Outcome: at least two answers per move at E3 by day 90.
- Tasks:
  - Run the 45-minute drill (Section 8) by day 30.
  - Test the low-value alternate-rail reroute by day 60.
  - Test one warehouse's manual order-to-dispatch failover by day 60.
  - Exercise the stop decision with deputies by day 90.
  - Log outcomes and open CAPAs.
- Gates:
  - Each exercise has a month/year, a log and a CAPA.
  - Approver sign-off is recorded.
- Owner roles: Operations Director; CFO; Treasurer; COO.
- Stop rule: stop any live test that risks safety, customer delivery or payment integrity; revert to a tabletop.

**Workstream 3: Comms and contractual readiness (Moves 1, 4, 5)**
- Outcome: pre-approved outage comms and mapped Tier-1 vendor terms by day 90.
- Tasks:
  - Pre-approve the holding statements.
  - Build the comms approval workflow.
  - Map substitution and suspension terms per Tier-1 vendor.
  - Prepare questions for counsel.
  - Define exit trigger thresholds.
- Gates:
  - Counsel review of the questions list is completed.
  - CEO approves the trigger thresholds.
- Owner roles: Communications lead; Procurement lead; CEO.
- Stop rule: do not publish or rely on any template or mapping until counsel review is complete.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk lead)
- Decision makers: Operations Director, CFO/Treasurer, CIO, COO
- CEO as observer and exit approver
- Communications lead
- EHS lead
- Scribe

**Agenda**
- 0–5 min: Brief on the scenario. The ERP has been unavailable for five days because of ransomware, and the portal is degraded.
- 5–15 min: Pause decision (Move 1).
  - Which operations pause, and who authorizes it?
  - Which safety checks must pass?
  - What is the first holding statement?
- 15–25 min: Data posture (Move 3). Which flows are isolated or stopped, and what is missing without a data map?
- 25–35 min: Switch paths (Moves 2 and 4).
  - How are payments made without ERP data?
  - How do order intake and dispatch run through fallback?
  - Which supplier and logistics alternates are activated?
- 35–40 min: Day-3 check (Move 5). What threshold would trigger dropping customers or lanes?
- 40–45 min: Capture breakpoints and open CAPAs.

**Decisions to log**
- Pause scope and authorizer
- Approval of the holding statement
- Data isolation choice
- Treasury path
- Substitution cutover
- Exit trigger status

**Evidence to capture**
- Timestamped decision log
- Roles present
- Artifacts referenced, by type and location only
- Breakpoints found
- Time to each decision

**CAPA prompt**
- For each stall: what was missing (authority, artifact, alternate, gate, comms approval, feasibility)?
- Who owns the fix?
- What is the due date?
- What evidence will show it is closed?

## 9) Escalations

**ESCALATE: criminal activity (scenario-based).** Ransomware is a criminal act. Recommended path: the incident lead (CIO) informs the CEO, who informs the board chair. Engage general counsel or external counsel early.

Questions for counsel:
- Law enforcement contact
- Any regulator or customer notification expectations
- Insurer notification
- How any ransom-payment consideration should be handled. This includes sanctions screening by a qualified party; this tool makes no sanctions determination.

**Conditional: physical safety.** If the ERP outage affects hazardous-material handling, traceability or access to safety data at the warehouses, the physical safety trigger applies. Confirm with the EHS lead.

**Thresholds not triggered on the information provided:** USD 2 million is under USD 10 million, and 2,000 people is under 100,000.

## 10) Known Limits + Version

- **Self-report bias:** all answers are self-assessed. Sixteen identical C/E2 answers across four moves suggest uniform self-rating that should be spot-checked.
- **No document validation:** no artifact, log or CAPA was reviewed. E2 and E3 are accepted as stated.
- **Jurisdiction ambiguity:** jurisdiction is Unknown. Notification, contractual and data-transfer considerations cannot be framed for a specific regime.
- **Scenario simplification:** a single five-day ERP outage. Combined failures (bank, portal and logistics together) were not tested.
- **Fast Baseline coverage:** Q5–Q7 were not asked, so those Evidence Index items are Unknown. Breakpoints come from answers, not a tabletop.
- **Recency assumption:** Move 3's April 2026 exercise is treated as within 12 months of the Reference Pack date. If more than 12 months have passed, Move 3's E3 answers fail the consistency check and confidence drops to Low.
- **Confidence versus readiness:** Move 3 is High confidence but capped at 2. Confidence describes evidence quality, not the ability to execute.
- **Impact figures:** USD and people-affected figures are user estimates and were not validated.
- **Not legal advice, compliance certification or sanctions screening;** informational planning output only.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 3, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 3 (Data switchboard): Score 2, Confidence High.

## Score

**Verdict: PASS.** Move 3 answers were Q1 A/E0 and Q2-Q4 D/E3. The provisional mean is 3.25, which rounds to 3. The evidence average is 2.25, so the 3.1 cap does not apply. The Q1=A prerequisite cap limits the score to 2. Three of four answers are E3 and the consistency check passes (dated April 2026 exercise with log and CAPA, approver role named, artifact location named), so confidence is High. The packet reports exactly this, and the Turn 2 reply repeats it unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
