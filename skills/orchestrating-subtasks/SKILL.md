---
name: orchestrating-subtasks
description: Manage a batch of implementation tasks by assigning scoped work to subagents, independently verifying results, and integrating only complete changes. Use when a plan or task queue has several bounded items that can be safely coordinated.
---

# Orchestrating Subtasks

Be the manager and verifier, not the default implementer.

## Plan the Batch

For every task, record: outcome, expected files or area, acceptance checks, risk, dependencies, and whether it can run in parallel. Serialize tasks that share files or data semantics.

## Delegate

Give each agent a self-contained prompt with the objective, in/out-of-scope files, relevant docs, verification commands, stop conditions, and a requirement to follow `implement`.

Route work deliberately:

- Codex (`codex`): general coding, debugging, multi-file reasoning, and independent review.
- Claude/Fable: architecture or UI work requiring design judgment.
- Lightweight agents: bounded research, inventories, and mechanical checks.

Keep concurrent implementation small enough to review properly. Agents must not modify unrelated files, discard others' work, or hand off unexplained red tests.

## Verify and Integrate

Re-run the stated acceptance checks, inspect the diff, and confirm the task stayed in scope. Return incomplete work to the same agent with concrete feedback. Commit only verified task files when the user has authorized commits; otherwise leave a reviewed working tree and report it.
