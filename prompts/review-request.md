# Review Request Template

Use this template when asking an AI assistant to review code changes.

---

## Summary

[One sentence describing what changed]

## Change Type

- [ ] Feature — New functionality
- [ ] Fix — Bug correction
- [ ] Refactor — Code improvement without behavior change
- [ ] Docs — Documentation only
- [ ] Test — Adding or updating tests
- [ ] Chore — Build, config, or dependency updates

## Files Changed

- `path/to/file1.ts` — [brief description of change]
- `path/to/file2.tsx` — [brief description of change]

## Review Focus

[What specifically you want feedback on]

- [ ] Correctness — Does the logic handle all cases?
- [ ] Security — Any vulnerabilities introduced?
- [ ] Performance — Any obvious inefficiencies?
- [ ] Standards — Does it follow project conventions?
- [ ] Testing — Is test coverage adequate?

## Context

[Any background the reviewer needs — why this approach, alternatives considered, etc.]

## Testing Done

- [ ] [Test 1 — what you verified]
- [ ] [Test 2 — what you verified]

---

## Example Usage

```markdown
## Summary

Add rate limiting to the authentication endpoints.

## Change Type

- [x] Feature — New functionality

## Files Changed

- `src/middleware/rateLimit.ts` — New rate limiting middleware
- `src/routes/auth.ts` — Applied middleware to login/register routes
- `src/config/limits.ts` — Rate limit configuration constants

## Review Focus

- [x] Security — Is the rate limiting implementation secure?
- [x] Performance — Any concerns with Redis lookups per request?
- [x] Standards — Does middleware pattern match existing code?

## Context

Implementing rate limiting to prevent brute force attacks on auth endpoints. Chose sliding window algorithm over fixed window for smoother limiting. Using Redis for distributed state across instances.

Alternatives considered:
- Token bucket — More complex, didn't need burst handling
- In-memory — Wouldn't work with multiple server instances

## Testing Done

- [x] Unit tests for rate limit logic
- [x] Integration test hitting limit and verifying 429 response
- [x] Manual test with Artillery load testing tool
```
