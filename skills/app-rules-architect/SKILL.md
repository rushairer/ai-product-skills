---
name: app-rules-architect
description: Extract, define, organize, and maintain reusable app product rules for software projects. Use when Codex should turn repeated UX or product decisions into durable rules, create or update files like APP_RULES.md, APP_RULES_TEMPLATE.md, PRODUCT_PRINCIPLES.md, or FEATURE_RULES.md, separate universal principles from project-specific behavior, review whether a feature violates existing rules, or help a team build a reusable product-method framework that can be reused across multiple apps.
---

# App Rules Architect

Treat product rules as a reusable system, not as scattered opinions.

## Goals

- Extract repeated product decisions into explicit rules.
- Separate universal rules from project-specific rules.
- Keep rules actionable for design, product, and engineering.
- Prevent future UI and interaction drift.

## Work In This Order

1. Identify repeated product decisions.
2. Group them by level: principle, app, or feature.
3. Separate universal guidance from local project rules.
4. Write the smallest useful ruleset.
5. Check whether the rules can guide future decisions.

## Rule Layers

Always classify rules into one of these layers:

- **Product Principles**
  - Cross-project rules.
  - Examples: success feedback should be visible; destructive actions need confirmation.

- **App Rules**
  - Rules for the current product.
  - Examples: apply actions return to the wheel; saved resources live in templates.

- **Feature Rules**
  - Rules for one complex module only.
  - Examples: import flows, editor flows, onboarding flows.

Do not mix all three layers into one document unless the project is tiny.

## Core Method

When creating or updating rules, always answer these:

1. What user outcome repeats here?
2. What decision keeps recurring?
3. Is this true for most apps, or only this app?
4. What should happen next time a similar case appears?

If the answer will likely repeat across projects, put it in a reusable template.
If the answer depends on this product’s information architecture, keep it project-specific.

## Common Rule Families

Look for rules in these areas first:

- success navigation
- success feedback
- save vs apply semantics
- destructive actions
- import and export flows
- empty states
- editing flows
- navigation ownership
- wording consistency
- list and library behavior

## Output Shape

Prefer this structure for project rules:

```md
# App Rules

## Success Navigation
## Success Feedback
## Destructive Actions
## Save Vs Apply
## Import / Export
## Empty States
## Editing Flows
## Consistency
## Engineering Pattern
```

Prefer this structure for reusable templates:

```md
# App Rules Template

## How To Use
## Product Principles
## App-Specific Decisions
## Feature Rules
## Review Checklist
```

## Writing Rules

Write rules so another Codex instance or teammate can apply them without guessing.

### Do

- Use direct, stable language.
- Explain the rule before giving examples.
- Show when the rule applies.
- Include a short decision rule.
- Include examples only when they reduce ambiguity.

### Don’t

- Write vague slogans with no operational meaning.
- Encode one-off edge cases as global rules.
- Mix product reasoning with implementation details too early.
- Copy current UI text into the rules unless wording is part of the rule.

## Decision Rules

- If a rule helps many apps, treat it as a principle.
- If a rule depends on a product’s tabs, resources, or workflow, treat it as app-specific.
- If a rule only matters inside one surface, treat it as a feature rule.
- If a rule keeps being broken in implementation, add an engineering pattern section.

## Review Existing Rules

When reviewing an existing `APP_RULES.md`, check:

1. Are any rules actually universal principles?
2. Are any rules too specific and better moved to feature rules?
3. Are any rules duplicated in multiple sections?
4. Can a new feature owner use the rules to make a decision quickly?

## Update Workflow

When the user asks to update rules:

1. Find the repeated decision or inconsistency.
2. Confirm whether it is a principle, app rule, or feature rule.
3. Update the smallest document that should own it.
4. Add examples only if the rule is likely to be misunderstood.
5. Suggest follow-up review of affected screens or flows.

## Recommended Outputs

Depending on the task, produce one of:

- `APP_RULES.md`
- `APP_RULES_TEMPLATE.md`
- `FEATURE_RULES.md`
- a short gap analysis between existing behavior and current rules
- a proposed refactor plan for inconsistent flows

## Good Triggers

This skill is especially useful when the user asks things like:

- “Should this be a general rule or only for this app?”
- “Can this product rule be reused in other projects?”
- “Help me turn these decisions into a reusable framework.”
- “Create an app rules template.”
- “Review whether this new feature violates existing app rules.”
