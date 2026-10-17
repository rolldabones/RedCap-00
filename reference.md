# RedCap-00 Reference Pack

**Reference · RedCap-00 v1.2.0 · 18 October 2026 (KST) · text of record**

Supply this whole file with the instruction block in [instructions.md](instructions.md). It was the GPT's knowledge file, published until v1.1.4 inside the README as `RedCap-00_Reference_v0.1.md`; it now stands as its own file. The changes are listed in [CHANGELOG.md](CHANGELOG.md) v1.2.0.

**Artifact:** RedCap-00 Reference Pack  
**Version:** v1.2.0 (formerly v0.1; see [CHANGELOG.md](CHANGELOG.md) v1.2.0)  
**Purpose:** Canonical question bank, scoring method and output schema for the RedCap-00 Optionality Self-Check. The regression harness is in [tests.md](tests.md).  
**Use rule:** The assistant running [instructions.md](instructions.md) must follow this file exactly. No new sections. No new question themes.

---

## 1) A to D Semantics (consistent across all questions)

- **A (pattern score = 1):** None, unknown, ad hoc, person-dependent
- **B (pattern score = 2):** Partial, informal, inconsistent, untested
- **C (pattern score = 3):** Documented, owned, repeatable, limited or no recent testing
- **D (pattern score = 4):** Tested in last 12 months with logs and CAPA, alternates viable, approvals and comms ready

**Answer format per question (mandatory):**

- `Answer: [A|B|C|D]`
- `Evidence: [E0|E1|E2|E3]`
- `Clarifier: (optional, <= 40 words, no sensitive data)`

---

## 2) Evidence Levels E0 to E3 (strict definitions)

- **E0 (evidence score = 0) No evidence:** No artifact, no owner, no record
- **E1 (evidence score = 1) Verbal only:** People say it exists, but no artifact named and no owner identified
- **E2 (evidence score = 2) Documented + owned:** A named artifact exists and a named owner role can produce it (policy, runbook, clause summary, checklist, control description)
- **E3 (evidence score = 3) Tested + logged + CAPA:** Exercised within last 12 months in a tabletop/drill/simulation with logged outcomes and at least one follow-up action (CAPA)

**Anti-inflation definitions (must enforce):**

- “Documented” requires **artifact type + owner role**.
- “Tested” requires **month/year + log existence + CAPA existence**.
- “Alternate” requires **viable within 72 hours**, not “possible someday.”

---

## 3) Conservative Caps (hard caps)

### 3.1 Evidence-average cap

- Compute the move’s **evidence average**: the mean of its evidence scores (Section 2: E0=0, E1=1, E2=2, E3=3) across all of the move’s answers, not rounded.
- If the **evidence average is below 2** (below E2), cap that move’s score at **2**.

### 3.2 Prerequisite caps (existence tests)

Each move has one prerequisite question. If that question is answered **A**, cap the move’s score at **2**. Any other answer leaves the move uncapped by this section.

- **Move 1 Safe pause:** Q1 Stop authority clarity answered A (none or unclear)
- **Move 2 Treasury reroute:** Q1 Alternate banks and rails answered A (none)
- **Move 3 Data switchboard:** Q1 Tier-1 data flow map answered A (none)
- **Move 4 Substitution:** Q2 Qualified alternates answered A (none)
- **Move 5 Market exit:** Q1 Exit plan answered A (none)

---

## 4) Confidence Rules (per move)

Counts are taken over the move’s answers: 4 in Fast Baseline, 7 in Deepening. “More than half” means 3 or more of 4, or 4 or more of 7.

- **High:** more than half of the answers at **E3** and the move’s consistency check passes (Section 5.2)
- **Medium:** not High; more than half of the answers at **E2 or E3**, at least one answer at **E3**, and the move’s consistency check passes
- **Low:** otherwise

Raising the evidence level of any answer never lowers confidence.

**Confidence downgrade rule:**

- If the move’s consistency check fails (Section 5.2), set confidence to **Low** for that move.

---

## 5) Modes and Flow (reference behavior)

### 5.1 Modes

- **Fast Baseline:** Ask **Q1–Q4** for each move (20 questions total)
- **Deepening:** Ask **Q1–Q7** for each move (35 questions total) **plus** the mini tabletop (Section 6)

### 5.2 Mandatory consistency checks (asked after Fast Baseline)

Ask and record, for each move:

1. **Last exercise date** (month/year) and whether a log and a CAPA exist, for each move with any **E3** answer
2. **Approver role** for the move’s decision (Move 1 stop, Move 2 reroute, Move 3 data switch or clean stop, Move 4 substitution cutover, Move 5 exit)
3. **Artifact location** (general system, no links) for the move’s E2 and E3 artifacts

A move’s consistency check **passes** unless one of these holds:

- an E3 answer lacks a month/year within the last 12 months, a log or a CAPA
- the move has an E2 or E3 answer and no approver role can be named
- the move has an E2 or E3 answer and no artifact location can be named

A move with no E2 or E3 answer passes; its confidence is Low under Section 4 in any case. If a move’s check fails, downgrade that move’s confidence to Low (Section 4).

---

## 6) Mini Tabletop Script (Deepening mode only)

**Goal:** Reveal execution stalls and generate breakpoint candidates.

### 6.1 Time windows and decisions (exact)

- **0–6 hours decision:** What do you pause now, who authorizes it, what safety checks must pass, what is the first holding statement
- **6–24 hours decision:** Which switch path is chosen (rail, vendor, data posture, logistics), what gates must pass, who signs off
- **24–72 hours decision:** What is executed, what is monitored, what evidence is captured, what CAPA is opened

### 6.2 Breakpoint mapping rule

Breakpoints must be mapped to:

- **Time window:** 0–6 or 6–24 or 24–72
- **Impacted move(s):** 1–5
- **What breaks:** missing authority, missing artifact, missing alternate, missing gate, comms approval delay, operational infeasibility
- **Why it blocks execution:** one sentence

---

## 7) Forced-choice Question Bank (canonical)

### Move 1: Safe pause (ship, service, production)

**Q1 Stop authority clarity**

- A none or unclear
- B informal person-dependent
- C documented authority matrix
- D delegated authority exercised and logged

**Q2 Safety and continuity checks**

- A none
- B partial inconsistent
- C documented checklist plus rollback plan
- D tested checklist plus rollback plus criteria

**Q3 Communications readiness**

- A none
- B ad hoc drafts
- C templates exist for internal, customer, regulator
- D templates pre-approved with workflow and owners

**Q4 Contractual suspension basis (planning-level)**

- A unknown
- B case-by-case
- C clause library or summary exists
- D mapped to Tier-1 contracts with triggers and notices

**Q5 Logging and audit trail**

- A none
- B partial notes
- C decision log exists with owners
- D immutable log with timestamps, roles, artifacts

**Q6 Resume criteria**

- A unclear
- B informal
- C documented resume plan
- D tested resume plan with gates

**Q7 Escalation under conflict**

- A unknown
- B ad hoc
- C escalation path documented
- D escalation path tested

---

### Move 2: Treasury reroute (payments and treasury flows)

**Q1 Alternate banks and rails**

- A none
- B identified only
- C pre-cleared
- D tested reroute path with evidence

**Q2 Freeze or hold playbook**

- A none
- B informal
- C documented
- D tested with roles and comms

**Q3 Counterparty tripwires (planning-level)**

- A none
- B manual checks
- C defined triggers plus escalation
- D monitored triggers and exercised escalation

**Q4 Execute within 72 hours**

- A no
- B uncertain
- C likely
- D proven by exercise

**Q5 KYC or KYB readiness (high level)**

- A unknown
- B scattered
- C bundle exists
- D bundle maintained and rehearsed

**Q6 Letters of credit or alternate settlement paths**

- A none
- B ad hoc
- C playbook exists
- D playbook tested

**Q7 Treasury authority and backups**

- A unclear
- B informal
- C documented
- D delegated with backup and drilled

---

### Move 3: Data switchboard (move data lawfully or stop cleanly)

**Q1 Tier-1 data flow map (includes logs and telemetry)**

- A none
- B partial
- C documented
- D current and reviewed

**Q2 Transfer mechanism options identified (no determinations)**

- A unknown
- B case-by-case
- C options mapped
- D options mapped and exercised

**Q3 Segmentation, localization, shutdown runbook**

- A none
- B ad hoc
- C runbook exists
- D runbook tested

**Q4 Privileged and emergency access logging**

- A none
- B partial
- C documented
- D tested with audit trail

**Q5 Subprocessor awareness**

- A unknown
- B partial
- C documented list
- D monitored changes with review

**Q6 OT or critical access boundary**

- A unknown
- B informal
- C documented
- D tested emergency procedure

**Q7 Stop-cleanly retention and deletion procedure**

- A unknown
- B ad hoc
- C documented
- D tested on Tier-1 system

---

### Move 4: Substitution (suppliers, systems, banks, lanes, facilities)

**Q1 Tier-1 single points of failure**

- A unknown
- B partial list
- C ranked list
- D ranked list reviewed quarterly

**Q2 Qualified alternates**

- A none
- B possible but unqualified
- C identified and qualified
- D contractually and operationally viable within 72 hours

**Q3 Portability or failover plan**

- A none
- B informal
- C documented
- D tested in last 12 months

**Q4 Substitution or portability rights (high level)**

- A unknown
- B case-by-case
- C summarized
- D mapped for Tier-1 vendors

**Q5 Concentration limits**

- A none
- B informal
- C documented
- D monitored with triggers

**Q6 Logistics reroute options**

- A none
- B ad hoc
- C planned
- D exercised

**Q7 Cutover governance**

- A none
- B informal
- C gates exist
- D gates tested with evidence pack

---

### Move 5: Market exit (exit without burning the enterprise down)

**Q1 Exit plan across legal, ops, data, people, comms, support**

- A none
- B partial
- C documented
- D tested tabletop

**Q2 Trigger-based termination and unwind paths (high level)**

- A unknown
- B ad hoc
- C documented
- D rehearsed

**Q3 Customer obligations and support plan**

- A unknown
- B ad hoc
- C documented
- D scripts and comms workflow ready

**Q4 Data and people plan**

- A unknown
- B partial
- C documented
- D rehearsed responsibilities and steps

**Q5 Distributor or JV obligations**

- A none or unknown
- B partial
- C mapped
- D mapped with unwind plan

**Q6 Assets and IP handling**

- A unknown
- B ad hoc
- C documented
- D rehearsed approvals and steps

**Q7 Regulator and customer comms workflow**

- A none
- B ad hoc
- C templates
- D templates plus approval workflow

---

## 8) Scoring Method (deterministic)

### 8.1 Per-move provisional score

- Map answers to numeric: **A=1, B=2, C=3, D=4**.
- A question the user cannot or will not answer is recorded as **A** at **E0** (A covers unknown) and counts as an answer.
- Compute the **average** (arithmetic mean) of the move’s pattern scores across all of its answers.
- Round it to the nearest whole number. An exact half rounds **down**, the conservative direction: 2.5 → 2 and 3.5 → 3. Exact halves arise only in Fast Baseline (four answers); seven answers never average to an exact half.

### 8.2 Score = 0 condition (Unknown)

Set the move score to **0**, reported as **Unknown/Insufficient data**, if and only if more than half of the move’s answers are **A** at **E0** (3 or more of 4 in Fast Baseline; 4 or more of 7 in Deepening). When this zero rule applies, skip 8.1 and 8.3 for that move.

This is the only route to a score of 0 and the only case in which a move’s score is reported as Unknown/Insufficient data. Weak evidence that does not meet the zero rule is handled by the caps (Section 3) and by confidence (Section 4).

### 8.3 Apply caps

- Apply **Evidence-average cap** (Section 3.1)
- Apply **Prerequisite caps** (Section 3.2)
- Final score is the lower of the provisional score and any cap that applies. A move not zeroed under 8.2 therefore scores 1 to 4.

### 8.4 Evidence distribution

For each move, count: **#E0 #E1 #E2 #E3** across that move’s questions.

---

## 9) Output Packet Schema (exact)

In both modes the model output must contain **exactly 10 sections** with the headings below in order and must meet the count rules. Where a count differs by mode, both counts are stated.

1) **Snapshot**
   - Jurisdiction
   - Mode (Fast Baseline or Deepening)
   - Scenario tested
   - Tier-1 scope summary

2) **How Scoring Works**
   - Max **5 bullets** describing A–D, E0–E3, caps, confidence

3) **Scorecard**
   - For each of the 5 moves:
     - score 0–4
     - confidence High/Medium/Low
     - evidence distribution counts (#E0 #E1 #E2 #E3)
     - exactly **2 rationale bullets**

4) **Evidence Index**
   - For each move: list **5–8 artifact types**, label each: **Unknown, Claimed, Documented, Tested**
   - Artifact types are categories only, not content

5) **72-Hour Breakpoints**
   - Fast Baseline: exactly **5 bullets**, one per move, each drawn from that move’s weakest answer and marked “from answers, not exercised”
   - Deepening: exactly **10 bullets**, drawn from the mini tabletop (Section 6) and the answers
   - Each bullet includes: time window, impacted move(s), what breaks, why it blocks execution

6) **Top Blockers and Fixes**
   - Exactly **10 numbered items** in both modes, drawn from the answers (and in Deepening also from the tabletop)
   - Each includes: blocker, evidence gap, minimal fix (2 weeks), proper fix (6–12 weeks), owner role

7) **30/60/90-Day Plan**
   - Max **3 workstreams**
   - For each: outcome, tasks (3–6 bullets), gates (2–3 bullets), owner roles, stop rule

8) **Minimal Drill Script (45 minutes)**
   - Roles
   - Agenda
   - Decisions to log
   - Evidence to capture
   - CAPA prompt

9) **Escalations**
   - If triggers: list them and recommended executive/counsel escalation path
   - If none: “No escalation triggers identified from provided information.”

10) **Known Limits + Version**
   - Up to **10 bullets** including: self-report bias, no document validation, jurisdiction ambiguity, scenario simplification
   - End with exact footer: `RedCap-00 v1.2.0 | Evidence-capped scoring`

---

Final Liability rests with the Human.
