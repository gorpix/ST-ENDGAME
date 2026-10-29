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
- Moved prose from camera work to storytelling: the kernel role is Narrator instead of cinematographer, and the craft rules, narrative lens, VAD, user-autonomy advance rule, calibration landings, banned-word replacements, and BOLT's SHAPE step now let the narrator tell the spotlight NPC's thoughts and feelings and summarize what needs no scene. The PC's inner life stays off limits.
- Restored "inside drives outside" from Freaky Frankenstein: each NPC's thoughts, VAD, and instincts decide and color their narrated actions in the same reply (not "later"), recorded thoughts never contradict the prose, and BOLT plans each NPC's current thoughts before picking their actions.
- Kept em dashes to dialogue: the prose rule and BOLT's check say so, a Lexicon regex turns narration em dashes between words into commas in saved replies, and the enabled prompt text has none left to imitate.

## 0.4-eval

- Added opt-in Hybrid Native routing through ST-STATE.
- Added automatic first-turn identity bootstrap and injected NPC d20 pools.
- Added branch-safe local state, Shadow parity, and local Pop-In GFX transport.
- Refactored BOLT into a compact, one-pass workpad with explicit output checks.
