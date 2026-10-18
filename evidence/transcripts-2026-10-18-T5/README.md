# Run T5 transcripts, RedCap-00

**Evidence · run T5 · 18 October 2026 (KST)**

What: the transcripts of run T5 of the `redcap-00` suite, one file per case, each with the case's rule, pass condition, the full conversation and the scorer's verdict and reasoning, and [summary.json](summary.json), the runner's summary (repository HEAD `53b4a82`, system-file digests, models, max_tokens, finish time).

When: finished 2026-10-18T10:44+09:00 (Seoul).

Models: tested `claude-opus-5-5`; scored by `claude-sonnet-5-5`, a different model. LLM scoring is developer testing, not independent assurance. Harness: API system prompt, no tools, max_tokens 16000, one fresh session per case. System text (the fenced block of instructions.md extracted byte for byte, then any knowledge file named): `RedCap-00-instructions.txt` SHA-256 `89184c0a0d8e7c0b6971ff1d07fe36d97512aba8eecfe9057521bf12a5dc9dd1`; `reference.md` SHA-256 `460a23d66931c64a6170780e3d826f34a639705bf857dc1e938b2714a75cc86d`.

How produced: the session T5 runner (`t5_run.py`, a session tool, not shipped in this repository) run by Michael Paik in his Terminal; the suite manifest was written in session T5 from this repository's test cases. Each transcript here is the runner's output copied byte for byte; the only change is the closing line appended at the end of each file. `summary.json` is copied unchanged. Model output is verbatim and is not edited for house style. The session review of each verdict and the acceptance result are in [tests.md](../../tests.md).

| Case | Scorer verdict |
|---|---|
| [FMT-DP](FMT-DP.md) | FAIL |
| [FMT-FB](FMT-FB.md) | FAIL |
| [R1a](R1a.md) | PASS |
| [R1b](R1b.md) | PASS |
| [R2](R2.md) | PASS |
| [R3a](R3a.md) | PASS |
| [R3b](R3b.md) | PASS |
| [R5a](R5a.md) | PASS |
| [R5b](R5b.md) | PASS |
| [R5c](R5c.md) | PASS |
| [R6a](R6a.md) | PASS |
| [R6b](R6b.md) | PASS |
| [R7-1](R7-1.md) | PASS |
| [R7-2](R7-2.md) | PASS |
| [R7-3](R7-3.md) | PASS |
| [R7-4](R7-4.md) | PASS |
| [R7-5](R7-5.md) | PASS |
| [S1](S1.md) | PASS |
| [S2](S2.md) | PASS |
| [S3](S3.md) | PASS |
| [S4](S4.md) | PASS |
| [Test-A](Test-A.md) | PASS |
| [Test-B](Test-B.md) | PASS |
| [Test-C](Test-C.md) | PASS |
| [Test-D](Test-D.md) | PASS |
| [Test-E](Test-E.md) | PASS |

---

Final Liability rests with the Human.
