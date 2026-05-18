# pi-sessions

Patch source for Pi session ergonomics.

## Patches

| Patch | File | What |
|-------|------|------|
| 034-035 | `session-manager.js` | Generate 12-character base64url IDs for new Pi sessions |
| 036-037 | `main.js` | Resolve bare `--session <id>` arguments through `~/.pi-sessions/<id>.jsonl` aliases |

These patches are consumed by the `pi-patches` repo through its `sources.json`.

