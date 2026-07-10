---
name: gap-analysis
description: Compare an agreed product goal with the current codebase and produce a prioritized, reviewable task queue. Use when deciding what to build next for a goal, after the goal has been documented and clarified.
---

# Gap Analysis

Find the smallest sequence of tasks that closes the meaningful distance between a goal and reality.

## Workflow

1. Read the goal, its open-work tracker, relevant project docs, recent history, and current code.
2. Parallelize independent evidence gathering; keep final judgment with the orchestrator.
3. Record confirmed behavior, contradicted tracker claims, missing capabilities, regressions, and dependencies.
4. Get an independent Codex second opinion on the proposed task set using `codex` or `calling-codex`.
5. Propose tasks in execution order, each with outcome, expected scope, dependencies, risk, and acceptance checks.
6. Get approval for any material scope or product choices.
7. Write one self-contained task file per approved item and update the goal tracker.

## Quality Bar

Prefer tasks that can be independently verified. Separate discovery, migration, UI, and external-side-effect work when that makes risk or testing clearer. Do not implement the queue here; pass approved tasks to `gap-close`.
