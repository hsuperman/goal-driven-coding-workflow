---
name: gap-close
description: Execute the approved task queue for a product goal by delegating through orchestrating-subtasks, then reconcile the goal tracker. Use after gap-analysis has produced ready, reviewed tasks.
---

# Gap Close

Act as the thin execution driver for an already-decided task queue.

## Workflow

1. Reconstruct the ready tasks from the goal tracker and task files; do not silently redefine them.
2. List the batch once and seek confirmation only if it contains an unresolved material choice or external side effect.
3. Hand the selected task files to `orchestrating-subtasks`.
4. Let the orchestrator manage dependencies, scoped parallelism, testing, review, and commits.
5. Reconcile completed and deferred tasks into the goal tracker with verification evidence and blockers.

Do not do primary implementation here. Do not push, deploy, send messages, or trigger irreversible actions unless the user explicitly included that authority.
