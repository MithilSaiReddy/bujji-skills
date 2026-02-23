# 🧩 Bujji Skills Marketplace

Community-maintained skill library for [Bujji](https://github.com/YOUR_USERNAME/bujji) — the lightweight personal AI assistant.

Skills are Markdown files that shape how Bujji behaves for specific tasks. Install them from the Bujji web UI in one click.

---

## How It Works

1. **Browse** skills in the Bujji web UI (🧩 Marketplace tab)
2. **Click Install** — Bujji fetches the `SKILL.md` from this repo and saves it locally
3. **Agent reloads** — the skill is active on your next message. No restart needed.

---

## Skill Catalog

<!-- AUTO-GENERATED — do not edit this section manually -->
<!-- Updated by CI on every merge to main -->

See [index.json](./index.json) for the machine-readable catalog.

---

## Contributing a Skill

Read [CONTRIBUTING.md](./CONTRIBUTING.md) — the short version:

```
skills/
  your-skill-name/
    SKILL.md       ← the instructions injected into bujji's system prompt
    meta.json      ← title, icon, tags, author
```

Open a PR. CI validates it. Maintainer merges. **Done — it's live in the marketplace.**

---

## Skill Guidelines

- One skill = one capability (focused beats broad)
- Write instructions in imperative mood: "Always...", "Return...", "When X, do Y"
- Under 800 words — the agent reads all active skills on every message
- No harmful, deceptive, or manipulative skills

---

## Stats

![Skills Count](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FYOUR_USERNAME%2Fbujji-skills%2Fmain%2Findex.json&query=count&label=skills&color=4ade80)

---

## License

Skills in this repo are published under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — freely usable, no attribution required.
