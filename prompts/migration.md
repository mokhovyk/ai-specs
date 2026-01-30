# Migration Template

Use this template when asking an AI assistant to upgrade dependencies or migrate to new patterns.

---

## Task

[One sentence describing the migration]

## Current State

- **Version/Pattern**: [What you're migrating from]
- **Scope**: [How many files/components affected]
- **Known issues**: [Any existing problems to address]

## Target State

- **Version/Pattern**: [What you're migrating to]
- **Breaking changes**: [Key differences to handle]
- **New capabilities**: [Features to adopt if relevant]

## Migration Strategy

- [ ] **Incremental** — Migrate file-by-file, keep both patterns temporarily
- [ ] **Big bang** — Migrate everything at once
- [ ] **Strangler fig** — New code uses new pattern, migrate old code gradually

## Files to Migrate

- `path/to/file1.ts`
- `path/to/file2.tsx`
- `src/components/**/*.tsx` (pattern)

## Constraints

- [ ] [Backward compatibility requirements]
- [ ] [Testing requirements]
- [ ] [Deployment considerations]

## Validation

- [ ] [How to verify migration succeeded]
- [ ] [Tests that must pass]
- [ ] [Manual verification steps]

---

## Example Usage

```markdown
## Task

Migrate from React Query v4 to TanStack Query v5.

## Current State

- **Version**: @tanstack/react-query 4.36.1
- **Scope**: 47 files using useQuery/useMutation
- **Known issues**: Some queries missing error boundaries

## Target State

- **Version**: @tanstack/react-query 5.x
- **Breaking changes**: 
  - `onSuccess`/`onError` callbacks removed from useQuery
  - New `useSuspenseQuery` for Suspense
  - `cacheTime` renamed to `gcTime`
- **New capabilities**: Improved TypeScript inference, streaming SSR

## Migration Strategy

- [x] **Incremental** — Migrate file-by-file

## Files to Migrate

- `src/hooks/queries/*.ts`
- `src/components/**/*.tsx` (files importing from @tanstack/react-query)

## Constraints

- [ ] Must maintain existing error handling behavior
- [ ] Cannot break production during migration
- [ ] All existing tests must pass

## Validation

- [ ] `npm run typecheck` passes
- [ ] `npm run test` passes
- [ ] Manual test of critical user flows
```
