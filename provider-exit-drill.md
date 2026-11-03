# The Provider Exit Drill

**Companion note · RedCap-00 v1.3.0 · 4 November 2026 (KST)**

RedCap-00 asks whether an organization can execute five moves within 72 hours under disruption: safe pause, treasury reroute, data switchboard, substitution of critical dependencies and clean market exit. This note takes one of those questions, whether a critical dependency can be substituted and the exit made cleanly, down to the unit at which most professionals meet it first: one person's or one team's AI tooling. The question does not change with scale. It is not whether a switch of provider is permitted or affordable but whether it would execute within tolerance, and nothing answers that except a rehearsal. In **GRCnext™** terms the drill is an Exit, built and tested before it is needed, at the scale of a desk.

The note does not change the instrument. The instruction block, the Reference Pack, the tests and the acceptance status recorded in [tests.md](tests.md) are as they were. The drill is scored by hand on the README's scales, and its result does not enter a RedCap-00 Output Packet.

## Custody is the lock-in

A subscription locks a professional in by price, and a price change is visible on the invoice the month it happens. Custody locks in by what has come to live inside the provider: the conversation history that holds the reasoning behind a draft, the project memory and custom instructions that hold the house style, the uploaded files that are now the only tidy copy, the skills, workflows and connectors built on that provider's platform and the habits of one model's register that the work has quietly adopted. None of that appears on an invoice. A custody loss becomes visible on the day you try to leave, which is the worst day to discover it, and the provider's terms, prices, models and policies can change on a day you did not choose.

Custody is also where the professional obligations sit. The Client's confidential material, the record a regulator or a court may later ask for and the evidence that a decision was taken by a person all have to be producible without the provider's cooperation. A professional who cannot produce them from outside the provider has not merely a switching cost but a gap in the record.

## The custody register

The first instrument is an inventory, kept outside every provider, of what the work depends on and where the copy outside the provider is. One row per item.

| Item | Where it lives inside the provider | Where the copy outside lives | Format | Last verified | Owner |
|---|---|---|---|---|---|
| Live matter files | Project uploads | Document store, path | Native and PDF | date | name |
| Standing instructions and house style | Custom instructions, project instructions | Text file in the repository | Markdown | date | name |
| Skills, workflows, prompts | Provider's skill or project store | Repository | Markdown, scripts | date | name |
| Reasoning and decisions on each matter | Conversation history | Project note, below | Markdown | date | name |
| Connectors and credentials | Provider's integrations | Credential manager; list of what is connected | List | date | name |

The register is the evidence that the exit exists. A row whose outside copy is blank, stale or unverified is the exit that would fail, and it is better found in the register than in the drill, and better found in the drill than on the day.

## The project note

The second instrument is a note per live matter, in plain text, kept outside every provider, from which any current model in any provider can continue the work tomorrow with no access to the old provider. The idea of such a note, a record kept outside every provider from which another model can pick up the work, is Nate B. Jones's, credited below; the fields here are the account's own, and the first four are the four elements of **Informed Intent**: purpose, authority, boundaries and exit, as stated in [DOCTRINE.md](https://github.com/rolldabones/rolldabones/blob/main/DOCTRINE.md), the account's single normative statement of the three doctrines. The note then records the sources, the decisions, the definition of done and the next action.

```
PROJECT NOTE: [Client, matter, short name]
Updated [date, KST] by [name]

PURPOSE      What the work is for and for whom. One paragraph.
AUTHORITY    Who answers for the work; who may change its scope.
BOUNDARIES   What must never leave which tenancy; the confidentiality
             class; jurisdictions; deadlines; the house rules that bind.
EXIT         What stopping looks like; what is handed back on exit,
             and to whom.
SOURCES      Where the authoritative inputs live, outside any provider,
             by path or link. Nothing cited only to a conversation.
DECISIONS    The rulings that fixed the shape of the work, dated, with
             the name of the person who made each.
DONE         What an acceptable result looks like; who accepts it.
NEXT         The next step, who takes it and what it needs.
```

A note that cannot be written is a finding: the reasoning lives only in a conversation, the sources only in an upload, the decisions only in memory. Writing the note is the cheapest exit test there is, and it is run every time the matter moves.

## The 30-minute exit test

The third instrument is the rehearsal. On one live matter, with a clock running:

1. Open a current model from a different provider, cold: no history, no memory, no uploads from the old provider.
2. Give it the project note and the sources named in the note, from their outside copies.
3. Ask for the next action named in the note.
4. Stop at 30 minutes.

The test passes if, within the 30 minutes, the new session produces the next deliverable to the definition of done in the note, with nothing retrieved from inside the old provider. Record the date, the matter, the providers on each side, the time to the first usable output, what the new session asked for that the note did not hold and every item that had to be fetched from inside the old provider. That last list is the custody leak, and each entry on it is a row to add or correct in the register. The length of the test follows Nate B. Jones's: half an hour, on one real piece of work, is enough to show whether the work can leave and short enough to be run without a project behind it.

Two things the test does not establish. It does not establish that the new provider's output is acceptable; that is the acceptance decision, taken under [The Definition of Done](https://github.com/rolldabones/definition-of-done), and a passed exit test with a worse deliverable is a finding about the work, not about the exit. And it does not establish that the old provider will delete what it holds, honor a contractual exit right or satisfy a data residency rule. Those are organizational moves among RedCap-00's five, and questions for counsel.

## The standing drill

The fourth instrument is the calendar. The test is run once a quarter on one matter chosen on the day, and again on any of four triggers: a change in the provider's terms or prices, the retirement of a model the work depends on, a change in the provider's policy on the use of what it holds and the onboarding of a new Client whose material raises the confidentiality class. Each run updates the register and produces one record. A drill that is scheduled and not run is scored as not run.

## Scoring, on the README's scales

Answer one question for the desk, as the instrument answers its twenty for the organization, and give an evidence level.

- **A** ad hoc or unknown: no register, no notes, no test
- **B** partial or informal: notes for some matters; outside copies exist for some items; no test run
- **C** documented and owned: a register and a note for every live matter, each with a named owner; no test in the last 12 months
- **D** tested: the 30-minute test run in the last 12 months, with its record and the follow-up actions it produced, on every provider the work depends on

Evidence levels as in the README: E0 none, E1 verbal only, E2 a documented artifact with an owner role, E3 tested in the last 12 months with logs and follow-up actions. The instrument's rule applies by hand: a desk that answers D at E1 is scored as the evidence allows, not as the answer claims. Confidence Low means the evidence is untested, not that it is weak.

## Occasion and credit

The occasion is Nate B. Jones's post of 2 September 2026 (Coordinated Universal Time, UTC; 3 September KST), "Switching AI Providers: The Real Cost Nobody Prices," at https://natesnewsletter.substack.com/p/switch-ai-providers, and his video of the same day, "OpenAI, NVIDIA And Anthropic Just Split. Here's How I'd Spend $20, $60 Or $200." (AI News & Strategy Daily, YouTube, https://www.youtube.com/watch?v=L9xXnPqVfnM). The post is paid; its public page, read on 4 November 2026 (KST), names in its subtitle what he keeps outside every provider and the test each expensive plan has to pass, and opens from a then-current case of a provider changing the deal for the users of a third-party tool, which is his example and is not re-examined here. His five-prompt audit is members-only and is neither cited nor linked; nothing from the paid text or the audit is reproduced. What is his: custody as the lock-in that matters, the note kept outside every provider from which another model can continue, the 30-minute test on one real piece of work and the standing drill that keeps the test true. What is this repository's: the register, the fields of the note, the four triggers, the two things the test does not establish and the scoring on RedCap-00's scales.

Related, in this account: the Exit as a GRCnext™ primitive, in [grc](https://github.com/rolldabones/grc); [*Slow AI for the Chief Legal Officer*](https://github.com/rolldabones/AI-Governance-Academy/blob/main/slow-ai-for-the-chief-legal-officer.md), which requires the exit to be designed and tested before it is needed; and [The Definition of Done](https://github.com/rolldabones/definition-of-done) for the acceptance decision the test leaves open.

---

Final Liability rests with the Human.
