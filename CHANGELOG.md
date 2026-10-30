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
- Restored Freaky Frankenstein's no-repeat rules as a `<no_repeat>` block: NPCs never parrot the PC's line, no recaps unless they drive the next action, no reused descriptions, gestures, openers, or jokes across the last 4 replies even reworded, and no one-word or stacked-negative drama formulas. BOLT's check points to it.
- Made the PC "you" in narration everywhere, even inside an NPC's point of view; the POV rule had only covered PC sensations, and v0.5 replies drifted into naming the PC in third person. BOLT now says "the PC" instead of naming them.
- Restored the David Foster Wallace voice from the live v0.4 preset (it had replaced the "maximalist observational" block there, but the repo never got that edit), spelled out as concrete traits, with a "readable heat" rule that keeps sex and fast action plain while the recursion moves into the NPC's head. The prose module is now "✒️ DFW Prose & Narrative Lens".
- Added the narrator's deadpan: an occasional single dry line the narrator infers from the scene (irony, understatement, absurd practical truth), kept inside the story's world, never voicing the PC, at most one per reply and skipped when forced. BOLT's SHAPE step considers it.
- Restored "inside drives outside" from Freaky Frankenstein: each NPC's thoughts, VAD, and instincts decide and color their narrated actions in the same reply (not "later"), recorded thoughts never contradict the prose, and BOLT plans each NPC's current thoughts before picking their actions.
- Restored SillyTavern's Post-History Instructions slot (`jailbreak`), empty and enabled after Chat History. The build had dropped it, which also blocked character cards' post-history instructions; the build now recreates it if the source lacks it. The README notes that some models need a different jailbreak than 🔞 Adult Mode, which can go there.
- Kept em dashes to dialogue: the prose rule and BOLT's check say so, a Lexicon regex turns narration em dashes between words into commas in saved replies, and the enabled prompt text has none left to imitate.

## 0.4-eval

- Added opt-in Hybrid Native routing through ST-STATE.
- Added automatic first-turn identity bootstrap and injected NPC d20 pools.
- Added branch-safe local state, Shadow parity, and local Pop-In GFX transport.
- Refactored BOLT into a compact, one-pass workpad with explicit output checks.
