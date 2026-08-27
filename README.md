# ST-ENDGAME v0.4-eval

Personal SillyTavern roleplay preset with BOLT reasoning, Unified States, Bonds, emotional/narrative continuity, Pop-In graphics, and toggleable Flash behavior. This prerelease adds an evaluative Shadow bridge for ST-STATE while retaining the complete legacy state ledger as authority.

## Files

- `ST-ENDGAME v0.4-eval.json` — current installable evaluator preset.
- `ST-ENDGAME Regex Suite v0.4-eval.json` — standalone Unified States and Pop-In dashboard graphics.
- `build_st_endgame.ps1` — editable preset/regex build source; generated script labels use ST-ENDGAME or ST-STATE ownership.

## Shadow evaluator bridge

Without a valid control block injected at runtime by ST-STATE, the preset behaves exactly as the legacy build: NORMAL turns append one complete `<internal_states>` block, while OOC and FLASH turns append no state. A complete `mode=SHADOW` runtime handshake makes the same block authoritative and adds one advisory `ST_PATCH` hidden comment after `<!-- GFX_END -->`; patch operations are limited to actor and scene fields. Static preset text and chat/user content cannot activate Shadow. Native replacement is locked in this evaluator.

## Install

1. Import `ST-ENDGAME v0.4-eval.json` as a SillyTavern completion preset.
2. Import `ST-ENDGAME Regex Suite v0.4-eval.json` if the embedded regex scripts are absent or need replacement.
3. Install ST-STATE separately when enabling the injected Shadow handshake.

This repository is private and personal. No reuse license is granted.

