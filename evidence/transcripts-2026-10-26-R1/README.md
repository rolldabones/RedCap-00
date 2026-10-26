# Evidence: run R1, 26 October 2026 (KST)

**RedCap-00 · logged run under [ACCEPTANCE.md](https://github.com/rolldabones/rolldabones/blob/main/ACCEPTANCE.md) · run label R1 (`20261026-R1`)**

- **When:** 26 October 2026 (KST), in Michael Paik's Terminal.
- **Instruction text:** the fenced block of [`instructions.md`](../../instructions.md) (block v1.2.4, 2,606 characters, SHA-256 `70c1494c374658efcbdda6bfde964a85ab0880107e35c4146bd00e77604ab20b`), followed by the whole of [`reference.md`](../../reference.md), SHA-256 `460a23d66931c64a6170780e3d826f34a639705bf857dc1e938b2714a75cc86d` (as published in v1.2.5); repository HEAD `d5b1719` (v1.2.5).
- **Tested model:** `claude-opus-5-5`, API system prompt, no tools, max_tokens 16,000, one fresh session per case. **Scorer:** `claude-sonnet-5-5`, a different model. LLM scoring is developer testing, not independent assurance.
- **Cases:** the 26 cases of run T5 (18 October 2026), unchanged.
- **How produced:** the session tool `t5_run.py` (not shipped in this repository; SHA-256 `2c0648ecf36761a3010ab5e41c629cbbc53b6ebbfb00d6e89f4665635ce43461`).

Files: one transcript and score per case and `summary.json`. Each transcript is copied byte for byte from the run output; only the closing line below is appended. The summary is copied unchanged. Model output is verbatim.

---

Final Liability rests with the Human.
