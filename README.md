# ST-ENDGAME v0.4-eval

SillyTavern roleplay preset with BOLT reasoning, durable state, relationship continuity, local Pop-In GFX, and optional FLASH routing.

## Contents

- `ST-ENDGAME v0.4-eval.json` — importable completion preset.
- `ST-ENDGAME Regex Suite v0.4-eval.json` — optional dashboard and GFX regex scripts.
- `build_st_endgame.ps1` — editable preset builder.

## Modes

- `LEGACY` — complete `<internal_states>` output; default and inert without ST-STATE.
- `SHADOW` — ST-STATE validates a candidate patch while the legacy ledger remains authoritative.
- `NATIVE` — ST-STATE locally owns actor, scene, turn, and numeric relationship updates.

Native is evaluative. Unsupported state domains remain compatibility-backed; see [ST-STATE](https://github.com/gorpix/ST-STATE).

## Install

1. Import `ST-ENDGAME v0.4-eval.json` into SillyTavern.
2. Install and enable ST-STATE for Shadow or Native operation.
3. Import the Regex Suite only if the preset does not already contain its scripts.

## Development

Edit the source sections in `build_st_endgame.ps1`, then build and inspect the generated preset before importing it.

## License

No reuse license is granted for this personal preset.
