# Feature Request Template

Use this template when asking an AI assistant to implement a new feature.

---

## Task

[One sentence describing what you want to build]

## Context

- **Location**: [Where this feature should live in the codebase]
- **Dependencies**: [Existing code, hooks, or utilities to use]
- **Constraints**: [Technical or business limitations]

## Requirements

- [ ] [Functional requirement 1]
- [ ] [Functional requirement 2]
- [ ] [Non-functional requirement (performance, accessibility, etc.)]

## Inputs

Reference files the AI should read:

- `path/to/related/component.tsx`
- `path/to/similar/feature.ts`

## Expected Output

- [ ] [Primary deliverable]
- [ ] [Secondary deliverable]
- [ ] [Tests or documentation if needed]

## Example

[Optional: Show what success looks like — a UI mockup description, API response shape, or behavior description]

---

## Example Usage

```markdown
## Task

Add a dark mode toggle to the settings page.

## Context

- **Location**: `src/pages/Settings.tsx`
- **Dependencies**: `useTheme` hook from `@/hooks/useTheme`
- **Constraints**: Must persist to localStorage, no external dependencies

## Requirements

- [ ] Toggle switch component in settings UI
- [ ] Persists user preference across sessions
- [ ] Respects system preference as default

## Inputs

- `src/pages/Settings.tsx`
- `src/hooks/useTheme.ts`
- `src/components/ui/Switch.tsx`

## Expected Output

- [ ] Modified Settings.tsx with toggle
- [ ] Updated useTheme if needed
- [ ] No new dependencies added
```
