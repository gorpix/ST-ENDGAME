# ST-ENDGAME v0.5

SillyTavern roleplay preset with a short BOLT turn plan, durable state, relationship continuity, local Pop-In GFX, and optional FLASH routing.

## Contents

- `ST-ENDGAME v0.5.json` — importable completion preset.
- `ST-ENDGAME Regex Suite v0.5.json` — optional dashboard and GFX regex scripts.
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
4. Using ST-STATE in SHADOW or NATIVE mode? Also enable the **🖼️ Pop-In Graphics (enable with ST-STATE)** prompt. It is off by default because GFX does nothing in LEGACY mode.

## Development

Edit `build_st_endgame.ps1`, then build and inspect the generated preset before importing it. The script works in Windows PowerShell 5.1 and PowerShell 7; keep it saved as UTF-8 with BOM.

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File build_st_endgame.ps1 -Source "ST-ENDGAME v0.5.json" -Output "ST-ENDGAME v0.5.json" -RegexOutput "ST-ENDGAME Regex Suite v0.5.json"
```

`-Source` supplies the base settings, prompt order, kernel, and scene-intro blocks. Every other prompt (BOLT, FLASH, State Engine, prose modules, GFX) is defined in the script and overwrites the source.

## License

No reuse license is granted for this personal preset.
