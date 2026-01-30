# Bug Fix Template

Use this template when asking an AI assistant to diagnose and fix a bug.

---

## Problem

[One sentence describing the bug]

## Observed Behavior

[What actually happens — include error messages, screenshots, or logs]

## Expected Behavior

[What should happen instead]

## Reproduction Steps

1. [Step 1]
2. [Step 2]
3. [Step 3]

## Environment

- **Browser/Runtime**: [e.g., Chrome 120, Node 20]
- **OS**: [e.g., macOS 14, Windows 11]
- **Relevant versions**: [e.g., React 18.2, TypeScript 5.3]

## Relevant Files

- `path/to/suspected/file.ts`
- `path/to/related/file.tsx`

## Constraints

- [ ] [Any limitations on the fix approach]
- [ ] [Areas of code not to modify]

---

## Example Usage

```markdown
## Problem

Login form submits twice when clicking the submit button.

## Observed Behavior

Network tab shows two POST requests to `/api/auth/login`. Sometimes causes "user already logged in" error.

## Expected Behavior

Single POST request per form submission.

## Reproduction Steps

1. Navigate to `/login`
2. Enter valid credentials
3. Click "Sign In" button
4. Check Network tab — two requests visible

## Environment

- **Browser**: Chrome 120
- **OS**: macOS 14.2
- **Versions**: React 18.2, React Hook Form 7.49

## Relevant Files

- `src/pages/Login.tsx`
- `src/components/forms/LoginForm.tsx`
- `src/hooks/useAuth.ts`

## Constraints

- [ ] Cannot change the auth API
- [ ] Must maintain form validation behavior
```
