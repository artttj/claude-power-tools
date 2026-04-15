# Example: Debugging a Production Issue

## Scenario

Users report intermittent 500 errors on the checkout endpoint.

## Workflow

### Step 1: Activate Systematic Debugging

```bash
/systematic-debugging Intermittent 500 errors on /api/checkout
```

### Step 2: Follow the Process

The skill guides you through:

1. **Gather Context**
   - Check logs for error patterns
   - Note frequency and timing
   - Identify affected users/regions

2. **Form Hypotheses**
   - Race condition in inventory check
   - Database connection pool exhaustion
   - Third-party payment API timeout

3. **Test Each Hypothesis**
   - Review inventory locking code
   - Check connection pool metrics
   - Look at payment API response times

4. **Find Root Cause**
   - Payment API timing out after 5s
   - No fallback handling
   - Error propagates as 500

### Step 3: Fix and Verify

Use `/test-driven-development` to:
1. Add timeout handling
2. Implement fallback
3. Add circuit breaker pattern

Use `e2e-runner` to verify checkout flow works.

## Key Takeaway

Systematic debugging prevents guessing and ensures you fix the root cause, not just symptoms.
