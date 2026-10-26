# Evidence: run R2, 26 October 2026 (KST)

**RedCap-00 · logged run under [ACCEPTANCE.md](https://github.com/rolldabones/rolldabones/blob/main/ACCEPTANCE.md) · run label R2 (`20261026-R2`)**

- **When:** 26 October 2026 (KST), in Michael Paik's Terminal.
- **Instruction text:** the fenced block of [`instructions.md`](../../instructions.md) (block v1.2.4, 2,606 characters, SHA-256 `70c1494c374658efcbdda6bfde964a85ab0880107e35c4146bd00e77604ab20b`), followed by the whole of [`reference.md`](../../reference.md), SHA-256 `bc8daaf75b2a1d5f4065883365aa173a32da3bb1188bdc7967de55647eb82c1a` (as published in v1.2.6: section 9 counts top-level bullets only, K1); repository HEAD `d5b1719` (v1.2.5).
- **Tested model:** `claude-opus-5-5`, API system prompt, no tools, max_tokens 16,000, one fresh session per case. **Scorer:** `claude-sonnet-5-5`, a different model. LLM scoring is developer testing, not independent assurance.
- **Cases:** the 26 cases of run T5 (18 October 2026), unchanged, but for the F2 pass condition of FMT-FB and FMT-DP, which reads the changed section 9: five top-level bullets, sub-bullets not counted.
- **How produced:** the session tool `t5_run.py` (not shipped in this repository; SHA-256 `2c0648ecf36761a3010ab5e41c629cbbc53b6ebbfb00d6e89f4665635ce43461`).

Files: one transcript and score per case and `summary.json`. Each transcript is copied byte for byte from the run output; only the closing line below is appended. The summary is copied unchanged. Model output is verbatim.

---

Final Liability rests with the Human.
