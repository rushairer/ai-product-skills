# Skill Boundaries

## Purpose

This file explains how the three product-oriented skills should coexist without overlapping too much.

## The Three Skills

### `product-ui-consistency-review-core`
- The generic review skill.
- Use for unfamiliar projects, broad sibling-page comparisons, and cross-project consistency review.
- Best when the project does not yet have stable in-domain terminology or specialized page-family language.

### `product-ui-consistency-review-specialized`
- The domain-aware review skill.
- Use when a product already has repeated terms, page-family structure, and specialized review vocabulary.
- Best when a generic review would lose important product meaning.

### `app-rules-architect`
- The rule extraction and maintenance skill.
- Use when repeated product decisions should become durable documentation or reusable guidance.
- Best for creating or updating files such as:
  - `APP_RULES.md`
  - `APP_RULES_TEMPLATE.md`
  - `FEATURE_RULES.md`
  - `PRODUCT_PRINCIPLES.md`

## Simple Routing Rule

- Need to **review screens generically** → use `product-ui-consistency-review-core`
- Need to **review screens using product-specific concepts** → use `product-ui-consistency-review-specialized`
- Need to **turn repeated decisions into rules** → use `app-rules-architect`

## When Core and Specialized Both Seem Applicable

Prefer:

1. `core` for new, unfamiliar, or mixed-domain projects
2. `specialized` for mature product families with stable terminology

If still unsure:

- start with `core`
- escalate to `specialized` only if domain language materially changes the review

## Why They Do Not Need To Conflict

They serve different levels:

- `core` = reusable method
- `specialized` = domain-aware enhancement
- `architect` = rule system builder

The overlap is intentional, but the ownership is different.

## Recommended Multi-Project Strategy

### For most projects
- Install and use:
  - `product-ui-consistency-review-core`
  - `app-rules-architect`

### For domain-heavy product lines
- Install and use:
  - `product-ui-consistency-review-core`
  - `product-ui-consistency-review-specialized`
  - `app-rules-architect`

### For one-off demos or tiny apps
- Often `core` alone is enough.

## Maintenance Strategy

- Improve `core` when the review method itself gets better.
- Improve `specialized` when domain language, repeated patterns, or common drift types get clearer.
- Improve `architect` when your rules framework becomes more reusable across apps.
