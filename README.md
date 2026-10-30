# ST-ENDGAME v0.5

SillyTavern roleplay preset with a short BOLT turn plan, durable state, relationship continuity, local Pop-In GFX, and optional FLASH routing.

## Contents

- `ST-ENDGAME v0.5.json` — importable completion preset.
- `ST-ENDGAME Regex Suite v0.5.json` — optional dashboard, GFX, and lexicon regex scripts. The lexicon scripts rewrite "a beat" in the saved AI reply.
- `build_st_endgame.ps1` — editable preset builder.

## Modes

- `LEGACY` — complete `<internal_states>` output; default and inert without ST-STATE.
- `SHADOW` — ST-STATE validates a candidate patch while the legacy ledger remains authoritative.
- `NATIVE` — ST-STATE locally owns actor, scene, turn, and numeric relationship updates.

Native is evaluative. Unsupported state domains remain compatibility-backed; see [ST-STATE](https://github.com/gorpix/ST-STATE).

## Install

1. In **AI Response Configuration**, import `ST-ENDGAME v0.5.json` as a preset.
2. In SillyTavern's extensions panel, choose **Install extension**, enter `https://github.com/gorpix/ST-STATE`, and install/enable the extension.
3. Import the Regex Suite only if the preset does not already contain its scripts.
4. Pop-In GFX needs nothing in the preset: in SHADOW or NATIVE mode, ST-STATE (newer than 0.4.4-eval.3) adds the GFX rules itself while GFX is on in its settings.
5. Bring your own jailbreak if your model needs one: the preset ships none. Put it in the **Post-History Instructions** prompt (sent last, after BOLT) or in an in-chat Author's Note at depth 0 with the System role (sent just before BOLT). A character card's post-history instructions also fill that prompt.

## Development

Edit `build_st_endgame.ps1`, then build and inspect the generated preset before importing it. The script works in Windows PowerShell 5.1 and PowerShell 7; keep it saved as UTF-8 with BOM.

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File build_st_endgame.ps1 -Source "ST-ENDGAME v0.5.json" -Output "ST-ENDGAME v0.5.json" -RegexOutput "ST-ENDGAME Regex Suite v0.5.json"
```

`-Source` supplies the base settings, prompt order, kernel, and scene-intro blocks. Every other prompt (BOLT, FLASH, State Engine, prose modules) is defined in the script and overwrites the source.

## License

No reuse license is granted for this personal preset.
