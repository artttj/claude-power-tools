---
description: Alias — sharp code review via the code-reviewer agent
---

Dispatch the `code-reviewer` agent on the request below. Default scope: the current uncommitted diff (`git diff`) unless the user specifies otherwise. Report only high-confidence issues — bugs, security risks, clear standards violations. Skip stylistic nits and speculative concerns.

$ARGUMENTS
