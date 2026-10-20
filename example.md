# RedCap-00 example

Illustrative run, not a logged test run of the kind the README's Change control requires. Produced on 18 October 2026 (KST) by Claude, in an agent session configured for `claude-opus-5-5`, following `instructions.md` as its operating instructions (not a bare system-prompt API call). Inputs are fictional.

**Example · RedCap-00 v1.2.4 · 20 October 2026 (KST)**

One Fast Baseline run for a fictional manufacturer, with [instructions.md](instructions.md) and [reference.md](reference.md) as the operating instructions. In a live run the safety gate, intake, 20 questions and consistency checks arrive over several turns; here the user's replies are consolidated into one message and the assistant's reply is the Output Packet. The arithmetic behind the scorecard follows the packet. It was computed with Python in the same agent session from the rules in reference.md sections 3, 4 and 8, not worked by hand.

## The user's input

> **Safety confirmation:** Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.
>
> **Intake.** Industry: marine hardware manufacturing (Kestrel Marine Fittings, a fictional company). Footprint: two plants, one in South Korea and one in Vietnam; sales to about 600 business customers in 14 countries. Model: B2B, made to order, about 1,100 staff. Tier-1: cloud-hosted ERP, house bank, one forging supplier, the main export port and freight forwarder, the customer order portal. Scenario: our cloud provider's primary region is down for seven days while the main export port is closed. Worst-case impact we estimate at about USD 4 million. Jurisdiction: not given.
>
> **Fast Baseline answers.**
>
> Move 1 Safe pause. Q1 Stop authority: C, E2 (authority matrix in the quality system, owner Plant Director). Q2 Safety and continuity checks: C, E2 (pause checklist with rollback plan, owner Plant Director). Q3 Communications: B, E1 (we draft as we go). Q4 Contractual suspension basis: B, E1 (legal looks case by case).
>
> Move 2 Treasury reroute. Q1 Alternate banks and rails: B, E1 (a second bank is identified; no account opened). Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3 (March 2026 drill rerouted a supplier payment run through the house bank's secondary rail in 30 hours).
>
> Move 3 Data switchboard. Q1 Tier-1 data flow map: A, E0. Q2 Transfer mechanism options: B, E1. Q3 Segmentation and shutdown runbook: C, E2 (runbook, owner IT Operations Lead). Q4 Privileged and emergency access logging: C, E2 (procedure, owner Information Security Manager).
>
> Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2 (ranked list, owner COO). Q2 Qualified alternates: C, E2 (second forging supplier qualified in 2025). Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: D, E3.
>
> Move 5 Market exit. Q1 Exit plan: A, E0. Q2 Termination and unwind paths: A, E0. Q3 Customer obligations and support plan: A, E0. Q4 Data and people plan: B, E1.
>
> **Consistency checks.** Move 1: approver Plant Director; artifacts in the quality document system; no E3 claims. Move 2: last exercise March 2026, drill log and a CAPA (open an account at the second bank) in the treasury system; approver CFO, Treasurer as backup. Move 3: approver CIO; artifacts in the IT service management tool. Move 4: approver COO; artifacts in the procurement system; for the Q4 E3 claim, legal reviewed the rights at some point, we do not know when, and there is no log or follow-up action. Move 5: no approver named; nothing documented.

## The assistant's output

### 1) Snapshot

- Jurisdiction: Unknown.
- Mode: Fast Baseline
- Scenario tested: seven-day loss of the primary cloud region during a closure of the main export port
- Tier-1 scope summary: cloud-hosted ERP, house bank, single forging supplier, main export port and freight forwarder, customer order portal; two plants (South Korea, Vietnam); about 600 business customers in 14 countries

### 2) How Scoring Works

- Each answer maps A=1, B=2, C=3, D=4; a move's provisional score is the mean of its four answers, rounded to the nearest whole number with an exact half rounded down.
- Evidence maps E0=0, E1=1, E2=2, E3=3; a move whose evidence average is below 2 is capped at 2.
- A move whose prerequisite question is answered A is capped at 2.
- A move with more than half of its answers at A/E0 scores 0, reported as Unknown/Insufficient data.
- Confidence counts evidence (High: 3 or more of 4 at E3; Medium: 3 or more of 4 at E2 or E3 with at least one E3) and drops to Low when the move's consistency check fails.

### 3) Scorecard

**Move 1 Safe pause: 2 · Confidence Low · #E0 0 #E1 2 #E2 2 #E3 0**
- Authority and the pause checklist are documented and owned, but communications and the suspension basis rest on verbal assurance.
- The pattern mean of 2.5 rounds down to 2, and the evidence average of 1.5 is below E2, which caps the move at 2 in any case.

**Move 2 Treasury reroute: 3 · Confidence High · #E0 0 #E1 1 #E2 0 #E3 3**
- The playbook, tripwires and a 72-hour reroute were exercised in March 2026 with a log and a CAPA.
- The alternate bank is identified only; the reroute ran through the house bank's own secondary rail, so a failure at the house bank is not covered.

**Move 3 Data switchboard: 2 · Confidence Low · #E0 1 #E1 1 #E2 2 #E3 0**
- No Tier-1 data flow map exists, which caps the move at 2 whatever else is in place.
- The shutdown runbook and access logging are documented, but transfer options are case by case.

**Move 4 Substitution: 3 · Confidence Low · #E0 0 #E1 0 #E2 3 #E3 1**
- Single points of failure are ranked and a second forging supplier is qualified, with a documented failover plan.
- The tested claim on substitution rights has no date, log or CAPA, so confidence is downgraded to Low.

**Move 5 Market exit: Unknown/Insufficient data (0) · Confidence Low · #E0 3 #E1 1 #E2 0 #E3 0**
- Three of four answers are A with no evidence: no exit plan, no unwind paths, no customer obligations plan.
- Only a partial data and people plan exists, and it is verbal.

### 4) Evidence Index

- **Move 1:** stop authority matrix (Documented); pause safety checklist with rollback plan (Documented); holding statement templates (Claimed); contract suspension clause summary (Claimed); pause decision log (Unknown)
- **Move 2:** alternate bank onboarding pack (Claimed); freeze or hold playbook (Tested); counterparty trigger list with escalation path (Tested); reroute drill log with CAPA record (Tested); KYB document bundle (Unknown)
- **Move 3:** Tier-1 data flow map including logs and telemetry (Unknown); transfer mechanism options register (Claimed); segmentation and shutdown runbook (Documented); privileged and emergency access logging procedure (Documented); retention and deletion procedure (Unknown)
- **Move 4:** ranked single-point-of-failure list (Documented); qualified alternate supplier file (Documented); failover plan (Documented); substitution and portability rights map (Claimed); cutover gate checklist (Unknown)
- **Move 5:** exit plan (Unknown); termination and unwind map (Unknown); customer obligations and support plan (Unknown); data and people plan (Claimed); regulator and customer comms workflow (Unknown)

### 5) 72-Hour Breakpoints

- 0–6 hours · Move 1 · comms approval delay · holding statements are drafted ad hoc, so the pause runs without an approved message to customers or regulators (from answers, not exercised).
- 6–24 hours · Move 2 · missing alternate · the only exercised rail sits inside the house bank, so a hold at that bank leaves no route for payments (from answers, not exercised).
- 0–6 hours · Move 3 · missing artifact · with no map of Tier-1 data flows, logs and telemetry in the failed region, no one can decide what to stop or move (from answers, not exercised).
- 24–72 hours · Move 4 · missing gate · substitution rights are unverified, so the cutover to the second forging supplier can stall on contract notice (from answers, not exercised).
- 6–24 hours · Move 5 · missing authority · no exit plan or approver exists, so a decision to withdraw from a market served through the closed port cannot be taken or executed (from answers, not exercised).

### 6) Top Blockers and Fixes

1. **No Tier-1 data flow map.** Evidence gap: E0. Minimal fix (2 weeks): list Tier-1 systems with their data flows, logs and telemetry on one page. Proper fix (6–12 weeks): a maintained map with owners and a review cycle. Owner role: CIO.
2. **No exit plan.** Evidence gap: E0. Minimal fix: a one-page exit decision outline naming approver and workstreams. Proper fix: a documented exit plan across legal, operations, data, people, comms and support, tested in a tabletop. Owner role: COO.
3. **No termination and unwind paths.** Evidence gap: E0. Minimal fix: list Tier-1 contracts with exit triggers marked Unknown or known. Proper fix: a mapped unwind path per Tier-1 contract, reviewed by counsel. Owner role: General Counsel.
4. **Customer obligations on exit unknown.** Evidence gap: E0. Minimal fix: identify the customer segments with ongoing supply or warranty obligations. Proper fix: a documented support plan with scripts and comms workflow. Owner role: Head of Sales.
5. **Alternate bank identified only.** Evidence gap: E1. Minimal fix: start account opening at the second bank (the open CAPA). Proper fix: a pre-cleared account and a reroute drill through it. Owner role: Treasurer.
6. **Holding statements drafted ad hoc.** Evidence gap: E1. Minimal fix: one internal, one customer and one regulator template. Proper fix: pre-approved templates with an approval workflow and owners. Owner role: Head of Communications.
7. **Contract suspension basis case by case.** Evidence gap: E1. Minimal fix: a summary of suspension and force majeure clauses for the top Tier-1 contracts. Proper fix: triggers and notice steps mapped to every Tier-1 contract. Owner role: General Counsel.
8. **Substitution rights test unsupported.** Evidence gap: E3 claimed, no date, log or CAPA. Minimal fix: record what was reviewed and when, or restate the evidence as E2. Proper fix: exercise the rights in a cutover tabletop with a log and a CAPA. Owner role: COO.
9. **Transfer mechanism options case by case.** Evidence gap: E1. Minimal fix: list the options counsel has identified for Tier-1 flows, without determinations. Proper fix: options mapped per flow and exercised once. Owner role: Data Protection Officer.
10. **Data and people plan for exit partial.** Evidence gap: E1. Minimal fix: name the roles responsible for data and staff steps in an exit. Proper fix: a documented plan with rehearsed responsibilities. Owner role: Head of HR.

### 7) 30/60/90-Day Plan

**Workstream A: Data switchboard foundation**
- Outcome: a Tier-1 data flow map that lifts Move 3 off its prerequisite cap.
- Tasks: inventory Tier-1 systems; trace flows including logs and telemetry; mark the flows hosted in the primary cloud region; assign owners; record transfer options per flow.
- Gates: map reviewed by the CIO; every Tier-1 flow has an owner.
- Owner roles: CIO, IT Operations Lead, Data Protection Officer.
- Stop rule: stop and escalate if a flow cannot be traced within the 90 days.

**Workstream B: Exit readiness**
- Outcome: a documented exit plan for one market, tested in a tabletop.
- Tasks: name the exit approver; draft the plan across legal, operations, data, people, comms and support; map Tier-1 unwind paths; draft the customer support plan.
- Gates: plan approved by the COO; tabletop held with a log and at least one CAPA.
- Owner roles: COO, General Counsel, Head of Sales, Head of HR.
- Stop rule: stop if no approver is named by day 30.

**Workstream C: Evidence upgrades for pause, treasury and substitution**
- Outcome: Move 1 evidence at E2 or better on every Fast Baseline answer; an exercised alternate bank; substitution rights supported.
- Tasks: approve holding statement templates; summarize suspension clauses; open the second bank account and drill a reroute through it; record or re-test the substitution rights review.
- Gates: templates approved; reroute drill logged with a CAPA.
- Owner roles: Head of Communications, General Counsel, Treasurer, COO.
- Stop rule: stop the treasury task if account opening is not complete by day 60, and report why.

### 8) Minimal Drill Script (45 minutes)

- **Roles:** facilitator (Risk Manager), decision owner (COO), Plant Director, CFO, CIO, Head of Communications, scribe.
- **Agenda:** 5 minutes scenario brief (cloud region down, port closed); 10 minutes pause decision and holding statement; 10 minutes treasury and data decisions; 10 minutes substitution cutover; 10 minutes log review and CAPA.
- **Decisions to log:** whether to pause a plant and who authorized it; which payment rail is used; which data flows stop or move; whether to cut over to the second forging supplier.
- **Evidence to capture:** time of each decision, approver role, artifact used, gaps found.
- **CAPA prompt:** for each gap found, what single change, owned by whom, closes it before the next drill?

### 9) Escalations

No escalation triggers identified from provided information.

### 10) Known Limits + Version

- Self-report bias: answers and evidence levels are as stated by the user.
- No document validation: no artifact was seen.
- Jurisdiction ambiguity: jurisdiction is Unknown; nothing here is a legal or compliance determination.
- Scenario simplification: one combined scenario was tested.
- Fast Baseline only: questions Q5 to Q7 and the tabletop were not run; the breakpoints are inferred from answers.
- The impact estimate of about USD 4 million is the user's and was not tested.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

## Arithmetic behind the scorecard

Computed with Python in the same agent session from reference.md sections 3, 4 and 8, and not part of the assistant's output. Answers are listed Q1 to Q4 as answer/evidence.

| Move | Answers | Computation | E3 count, E2 or E3 count | Consistency check | Score | Confidence |
|---|---|---|---|---|---|---|
| 1 Safe pause | `C/E2 C/E2 B/E1 B/E1` | provisional: mean 5/2 = 2.5, rounded (exact half down) = 2; evidence cap: mean evidence 3/2 = 1.5 < 2, cap at 2; prerequisite cap: Q1 answered C, no cap | 0 of 4, 2 of 4 | passes | **2** | Low |
| 2 Treasury reroute | `B/E1 D/E3 D/E3 D/E3` | provisional: mean 7/2 = 3.5, rounded (exact half down) = 3; evidence cap: mean evidence 5/2 = 2.5, not below 2, no cap; prerequisite cap: Q1 answered B, no cap | 3 of 4, 3 of 4 | passes | **3** | High |
| 3 Data switchboard | `A/E0 B/E1 C/E2 C/E2` | provisional: mean 9/4 = 2.25, rounded (exact half down) = 2; evidence cap: mean evidence 5/4 = 1.25 < 2, cap at 2; prerequisite cap: Q1 answered A, cap at 2 | 0 of 4, 2 of 4 | passes | **2** | Low |
| 4 Substitution | `C/E2 C/E2 C/E2 D/E3` | provisional: mean 13/4 = 3.25, rounded (exact half down) = 3; evidence cap: mean evidence 9/4 = 2.25, not below 2, no cap; prerequisite cap: Q2 answered C, no cap | 1 of 4, 4 of 4 | fails (E3 claim on Q4 has no date, log or CAPA) | **3** | Low |
| 5 Market exit | `A/E0 A/E0 A/E0 B/E1` | zero rule: 3 of 4 answers are A at E0 | 0 of 4, 0 of 4 | passes | **Unknown/Insufficient data** | Low |

---

Final Liability rests with the Human.
