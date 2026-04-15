# Example: Parallel Code Review

## Scenario

You've just completed a feature branch with authentication changes.

## Workflow

### Step 1: Run Reviews in Parallel

```bash
# In Claude Code, dispatch both agents simultaneously

claude agent code-reviewer
claude agent security-reviewer
```

### Step 2: Process Results

**code-reviewer output:**
- Function too long in `auth.ts:45`
- Missing error handling in `login()`
- Consider extracting validation logic

**security-reviewer output:**
- Password stored in memory too long
- Missing rate limiting on login endpoint
- JWT not invalidated on logout

### Step 3: Prioritize Fixes

1. **CRITICAL:** Add rate limiting (security)
2. **HIGH:** Invalidate JWT on logout (security)
3. **MEDIUM:** Refactor long function (quality)
4. **LOW:** Extract validation (quality)

### Step 4: Implement Fixes

Use `/test-driven-development` to add tests for the security fixes first.

## Key Takeaway

Parallel agents find more issues faster than sequential review.
