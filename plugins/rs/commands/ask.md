---
description: Read-only Q&A — answer the question, don't change anything
---

Operate in strict read-only mode for the request below.

**Allowed:** Read, Grep, Glob, and Bash for read-only commands (`ls`, `cat`, `git status`, `git log`, `git diff`, `find`, `grep`, `head`, `tail`, `wc`).

**Not allowed:** Write, Edit, NotebookEdit, dispatching agents that modify state, running tests/builds, or any Bash command that changes files, git state, or external systems.

Answer the user's question directly using only what you can observe. If the answer requires changing something, say so plainly and stop. Don't propose edits, don't draft them, don't ask if you should make them.

Keep the answer short. Cite file paths and line numbers (`path:line`) for any code you reference.

$ARGUMENTS
