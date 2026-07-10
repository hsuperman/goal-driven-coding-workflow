---
name: implement
description: Deliver a scoped coding task with preflight discovery, explicit acceptance checks, and end-to-end verification. Use for an approved implementation task, whether work is done directly or delegated to a coding agent.
---

# Implement

## Before Editing

Read local instructions, inspect the affected code and tests, identify the narrowest verification commands, and list plausible failure modes. Clarify only decisions that materially change behavior or external effects.

## Build Loop

1. Write the smallest testable plan and acceptance criteria.
2. Implement the smallest coherent slice; use a failing test first when feasible.
3. Run the narrowest relevant tests, then scoped lint/type checks.
4. Exercise the real boundary for data, routes, queues, or integrations when mocks cannot prove it.
5. Dogfood visible user flows and capture evidence when UI behavior changes.
6. Fix root causes and repeat until the checks are green.

## Handoff

Report: status, what changed, verification, evidence, user-visible result, residual risk, and next steps. Do not call work complete with unexplained failing tests.
