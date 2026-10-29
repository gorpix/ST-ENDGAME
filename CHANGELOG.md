# Changelog

## 0.5

- Lowered reasoning effort from max to high.
- Replaced the 18-gate BOLT workpad with a 10-step plan of decisions (no drafted probes, per-turn checklist, or state-format rules), sent as an assistant message.
- Removed contradictory and dangling instructions (FLASH routing bias, prose calibration, `<dfw>`, `header`).
- SHADOW/NATIVE rules, including the Pop-In GFX format, now come only from ST-STATE's injected protocol; removed the preset's GFX prompt.
- BOLT and FLASH are defined in the build script instead of copied from the source preset; removed dead code and `-ActiveSettings`.
- Build script runs on Windows PowerShell 5.1 as well as PowerShell 7.
- Rewrote the banned vocabulary as grouped bans with replacements; narrowed `spine`, `meat`, and `slick` to their cliché uses and dropped `asset`, `vice`, and `breast`.
- Added Lexicon regex scripts that remove or rewrite "a beat" in saved AI replies.

## 0.4-eval

- Added opt-in Hybrid Native routing through ST-STATE.
- Added automatic first-turn identity bootstrap and injected NPC d20 pools.
- Added branch-safe local state, Shadow parity, and local Pop-In GFX transport.
- Refactored BOLT into a compact, one-pass workpad with explicit output checks.
