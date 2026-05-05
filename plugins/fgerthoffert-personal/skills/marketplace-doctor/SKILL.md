---
name: marketplace-doctor
description: Validate and fix GitHub Copilot CLI marketplace and plugin manifests for this repository. Use when marketplace registration, plugin installation, or skill discovery is failing.
user-invocable: true
---

# Marketplace Doctor

Audit and repair this repository so it works as a GitHub Copilot CLI marketplace and plugin source.

---

## What this skill does

1. Verify marketplace manifest(s) exist and are valid JSON.
2. Verify plugin manifest(s) exist and are valid JSON.
3. Confirm plugin metadata is consistent (name/version/description/skills path).
4. Confirm every skill has a `SKILL.md` with frontmatter `name`, `description`, and `user-invocable: true`.
5. Provide exact file-level fixes when anything is inconsistent.

---

## Expected file layout

- `.claude-plugin/marketplace.json`
- `.claude-plugin/plugin.json`
- `plugins/<plugin-name>/plugin.json`
- `plugins/<plugin-name>/skills/*/SKILL.md`

---

## Output requirements

When reporting results:

1. State pass/fail for each check.
2. List precise files to change.
3. Provide complete replacement snippets for broken JSON/frontmatter.
4. Include commands to verify:

```bash
copilot plugin marketplace add <owner/repo>
copilot plugin marketplace browse <marketplace-name>
copilot plugin install <plugin-name>@<marketplace-name>
copilot -p "/skills list" --allow-all-tools -s
```
