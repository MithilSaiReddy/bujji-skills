# Contributing a Skill to Bujji Marketplace

Anyone can add a skill. When your PR is merged, it's **instantly available** to all Bujji users in their marketplace tab.

---

## How to Submit

### 1. Fork this repo

### 2. Create a folder under `skills/`

The folder name is your skill's permanent ID. Use lowercase + hyphens only.

```
skills/
  your-skill-name/
    SKILL.md
    meta.json
```

### 3. Write `meta.json`

```json
{
  "id":          "your-skill-name",
  "title":       "Your Skill Title",
  "icon":        "🎯",
  "description": "One sentence: what does this skill make bujji do?",
  "tags":        ["writing", "productivity"],
  "author":      "your-github-username",
  "version":     "1.0.0"
}
```

**Rules:**
- `id` must exactly match your folder name
- `icon` must be a single emoji
- `tags` — pick from: `dev`, `code`, `data`, `writing`, `research`, `productivity`, `business`, `education`, `security`, `infra`, `creativity`, `git`
- `description` — max 120 characters, no period at the end

### 4. Write `SKILL.md`

This is the Markdown injected into bujji's system prompt when the skill is active. Write it as direct instructions to the agent.

**Template:**
```markdown
# Skill: Your Skill Title

## When to Use
[Describe the situation that triggers this skill]

## Behavior
- [Specific instruction 1]
- [Specific instruction 2]
- [Always / Never do X]

## Output Format
[How should bujji format its responses with this skill active?]

## Examples (optional but recommended)
User: [example request]
Bujji: [example response]
```

**Tips for writing effective skills:**
- Be specific. "Always use bullet points for lists" beats "be organised"
- Use imperative mood: "Return the code first, then explain" not "You should return..."
- Keep it focused — one skill = one capability
- Under 800 words. The agent reads all skills on every message

### 5. Open a PR

Title format: `skill: add your-skill-name`

The CI will automatically validate your `meta.json` and `SKILL.md`. Fix any errors flagged in the PR checks.

---

## What Gets Rejected

- Duplicate skills (check existing ones first)
- Skills that promote harmful, illegal, or unethical behaviour
- Skills with vague instructions ("be helpful" is not a skill)
- Skills that are just a system prompt override (e.g. "You are a pirate")
- Folder names with uppercase, spaces, or special characters

---

## Updating an Existing Skill

If you want to improve a skill you didn't author, open a PR with your changes. The original author will be tagged for review. If there's no response within 7 days, maintainers will review directly.

Version bump: patch fixes → `1.0.x`, new behaviour → `1.x.0`.

---

## Questions?

Open a [Discussion](../../discussions) — not an issue.
