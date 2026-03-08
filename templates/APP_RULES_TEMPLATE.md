# App Rules Template

## How To Use

- Use this file as a reusable starting point for a new project.
- Keep universal ideas short and stable.
- Replace bracketed placeholders with project-specific terms.
- Split out `FEATURE_RULES.md` when one module becomes complex.

## Product Principles

### Success Navigation
- After a successful action, take the user to the place where the result is active or easiest to verify.

### Success Feedback
- Every important success should be immediately visible through navigation, content change, message, haptic, or another clear signal.

### Destructive Actions
- Deleting, replacing, clearing, or overwriting meaningful user data should require clear confirmation.

### Save Vs Apply
- Saving to a library and applying to the current state are different actions and should be labeled and handled differently.

### Consistency
- Similar actions should use similar wording, placement, and outcomes across the app.

## App-Specific Decisions

### Primary Result Surface
- When users apply or activate content, send them to: `[result surface]`

### Library Surfaces
- Saved resources live in:
  - `[library A]`
  - `[library B]`

### Success Routing Rules
- `Apply -> [result surface]`
- `Save -> [library surface]`
- `Import and apply -> [result surface]`
- `Import only -> [library surface]`

### Main Navigation Ownership
- Top-level navigation is owned by: `[TabView / NavigationSplitView / custom router / other]`
- Child screens should request navigation through: `[environment action / router / callback / coordinator]`

## Common Rule Sections

### Success Navigation
- Describe where users land after successful create, save, import, apply, export, and delete flows.

### Success Feedback
- Define which actions rely on navigation as feedback and which need extra toast, banner, or haptic feedback.

### Destructive Actions
- List which flows need confirmation and what the confirmation must explain.

### Save Vs Apply
- Define where “save”, “apply”, “duplicate”, “import”, and “share” diverge in meaning.

### Import / Export
- Define preview requirements, overwrite behavior, and post-success destination.

### Empty States
- Define what each empty state must contain:
  - what is missing
  - why it matters
  - what the user should do next

### Editing Flows
- Define whether editing should dismiss, pop, stay in place, or redirect after success.

### Consistency
- Define stable wording and action hierarchy for repeated operations.

### Engineering Pattern
- Describe how the app should implement shared navigation and success handling so the product rules stay enforceable.

## Feature Rules

- Create `FEATURE_RULES.md` when a feature needs its own local behavior rules.
- Good candidates:
  - onboarding
  - import/export
  - editor flows
  - playback or execution flows
  - collaboration

## Review Checklist

- Can users immediately verify success?
- Is this action really “save” or actually “apply”?
- Is the destination consistent with similar actions?
- Does this flow need confirmation before destructive change?
- Does the empty state tell users what to do next?
- Would a new teammate make the same decision from these rules?

## Suggested Companion Files

- `APP_RULES.md`
- `FEATURE_RULES.md`
- `PRODUCT_PRINCIPLES.md`
- `UX_REVIEW_NOTES.md`
