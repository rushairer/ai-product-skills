# Rules and Skills README

## What Is Included

This repository now contains three related layers:

- **Project rules**
  - `PRODUCT_RULES.md`
  - `APP_RULES.md`

- **Reusable template**
  - `APP_RULES_TEMPLATE.md`

- **Skill drafts**
  - `SKILL_DRAFTS/app-rules-architect`
  - `SKILL_DRAFTS/product-ui-consistency-review-core`

- **Installer**
  - `install_skills.sh`

## What Each File Is For

### `PRODUCT_RULES.md`
- A lighter project-specific rules note.
- Useful as an early draft or quick reference.

### `APP_RULES.md`
- The main project-specific behavior rules.
- Use this as the source of truth for interaction decisions in this app.

### `APP_RULES_TEMPLATE.md`
- A reusable starting point for other projects.
- Copy it into a new app and replace placeholders with that app’s structure.

## What Each Skill Does

### `app-rules-architect`
- Extract repeated product decisions into durable rules.
- Separate universal principles from app-specific rules.
- Create or update files like:
  - `APP_RULES.md`
  - `APP_RULES_TEMPLATE.md`
  - `FEATURE_RULES.md`
  - `PRODUCT_PRINCIPLES.md`

### `product-ui-consistency-review-core`
- Review sibling screens and repeated flows for consistency.
- Check semantic, structural, interaction, and visual drift.
- Works as a project-agnostic core review skill.

## Recommended Usage Model

### In the current project
- Keep using `APP_RULES.md` as the project-specific rules file.
- Update it whenever repeated product decisions become stable.

### In a new project
- Start from `APP_RULES_TEMPLATE.md`.
- Copy and rename it to that project’s `APP_RULES.md`.
- Add feature-specific rule files only when needed.

### During design or implementation review
- Use `product-ui-consistency-review-core` to inspect sibling pages.
- Use `app-rules-architect` when a local decision should become a durable rule.

## How To Install the Skill Drafts

Run this from the repository root:

```bash
bash install_skills.sh
```

This installs the drafted skills into:

```bash
${CODEX_HOME:-~/.codex}/skills
```

After installation:

- Restart Codex or Xcode Coding Assistant.

## Recommended Evolution Path

1. Keep refining `APP_RULES.md` inside this project.
2. Reuse `APP_RULES_TEMPLATE.md` in other apps.
3. Improve `app-rules-architect` whenever you discover a repeatable rule workflow.
4. Improve `product-ui-consistency-review-core` whenever you find cross-project review patterns.
5. Keep project-specific review skills as enhanced layers on top of the core skill.

## Practical Rule of Thumb

- If it applies to many apps, put it in a reusable template or core skill.
- If it depends on this app’s tabs, pages, or flows, keep it in `APP_RULES.md`.
- If it only matters inside one module, move it to a feature-level rules file.
