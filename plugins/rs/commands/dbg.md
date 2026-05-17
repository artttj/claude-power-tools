---
description: Alias — systematic debugging via superpowers:systematic-debugging
---

Use the `superpowers:systematic-debugging` skill on the request below. Run it as-is — its discipline (reproduce first, hypothesize from evidence, change one variable at a time) is the whole point, so do not loosen or shortcut its checklist.

If `superpowers:systematic-debugging` is not installed, fall back to this evidence-first sequence:

1. **Reproduce.** Get the failure to happen on demand. State the exact command, input, environment, and observed output. If it can't be reproduced, that is the first bug to fix.
2. **Hypothesize from evidence.** Read the relevant code, logs, and recent diffs before guessing. Write down the smallest hypothesis the evidence supports. No speculative fixes.
3. **Test one variable at a time.** Change one thing, re-run the repro, observe. If it didn't change the outcome, revert and try the next hypothesis. Never stack untested changes.
4. **Report root cause.** When the bug is fixed, state what was actually wrong, why the fix works, and what (if anything) needs a regression test.

$ARGUMENTS
