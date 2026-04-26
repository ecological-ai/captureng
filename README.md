# captureng

Session-knowledge capture skill for Agents. Writes structured Markdown files preserving work, env variables, patterns, and decisions across sessions.

Three modes: **CREATE** (first full capture), **APPEND** (extend existing), **CHECKPOINT** (emergency partial under token pressure).

## Set of files

| File | Purpose |
|---|---|
| `SKILL.md` | Router — load order |
| `captureng-SKILL.md` | Content — capture template, modes, anti-recursive guard |
| `captureng.skill` | Packaged archive for upload to SKILL directory |
| `.github/workflows/build-skill.yml` | CI workflow — auto-builds and publishes `captureng.skill` on push |
| `README.md` | Explanatory instructions and overview for this software package |

## Install

- **claude.ai web platform:** upload `captureng.skill` via skill settings (recommended). Or add `captureng-SKILL.md` contents to Personal Preferences via `Settings > General`.

- **Claude Code desktop app:** copy contents of this folder into `~/.claude/skills/captureng/`.

- **Other platforms:** adapt this set of files to your `harness+model`. Star or Fork the git repo if you like. 

## When It Triggers

- "save this session", "capture session knowledge", "grab full session"
- "checkpoint this session", "how do I resume this work"
- Token budget below 20% of rate limit hit (under-triggers if capturing skill not already loaded)

## Peer Skills

Load on demand when task requires:

- **[prompteng](https://github.com/ecological-codes/prompteng)** — main set of rules + framework for doing better prompt engineering
- **[packageng](https://github.com/ecological-codes/packageng)** — `.skill` file validation + packaging
- **[safe-skill-creator](https://github.com/ecological-codes/safe-skill-creator)** — skill design + iteration

## Companion Files

Available in - **[ecological-codes/user-prefs](https://github.com/ecological-codes/user-prefs)**

- `agent.md` 

- `trusted-hosts.md` 

## Style Convention

Directives use the following section headers with numbered lists, shared across peer skills: 

- **[RULES]** — enforceable constraints applied at runtime.
- **[ACTIONS]** — autonomous steps agent executes in normal workflow.
- **[HUMAN ACTIONS]** — UI actions; agent skips, cannot delegate.

## License

See [LICENSE](./LICENSE). (C) Copyright 2026 - Sameer Khan - Various and Several Rights Reserved.

---
README.md v2.2.0 - Human Approved