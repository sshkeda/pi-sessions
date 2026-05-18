# pi-sessions

Quality-of-life patches for [Pi](https://github.com/earendil-works/pi-mono) session IDs.

Pi's default session IDs are long random tokens. After a while you accumulate dozens of session files and can't recall which is which. This repo gives them short readable handles you can pass on the command line.

## What you get

- **12-character base64url session IDs** for every new Pi session (e.g. `tXz7p_Q9Kw3a`) instead of long UUIDs.
- **Bare `--session <id>` resolution**: `pi --session tXz7p_Q9Kw3a` finds the right session file via `~/.pi-sessions/<id>.jsonl` aliases — no need to pass a full path.

## Patches

| Patch | File | What |
|-------|------|------|
| 034-035 | `session-manager.js` | Generate 12-character base64url IDs for new Pi sessions |
| 036-037 | `main.js` | Resolve bare `--session <id>` arguments through `~/.pi-sessions/<id>.jsonl` aliases |

## Install

These patches are consumed by the [`pi-patches`](https://github.com/sshkeda/pi-patches) repo via its `sources.json`. Install via:

```bash
git clone https://github.com/sshkeda/pi-patches
cd pi-patches
bash apply.sh
```

## License

MIT
