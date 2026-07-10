---
name: grill-for-unknowns
description: Stress-test a product goal, design, or implementation plan against codebase evidence before delegating or building. Use when the direction seems plausible but hidden assumptions, scope gaps, dependencies, or verification risks could cause wasted work.
---

# Grill for Unknowns

Turn a plausible plan into an evidence-backed launch packet.

## Method

1. State the intended outcome and the decision the plan is meant to support.
2. Build a small map of affected users, systems, data, interfaces, and ownership boundaries.
3. Compare the map with the actual repository, docs, and current runtime behavior where available.
4. Surface unknowns in four groups: product intent, technical behavior, operational dependencies, and verification.
5. Classify each unknown as resolved, safe assumption, blocker, or deliberate decision.
6. Tighten the scope, acceptance criteria, rollback/deviation policy, and proof required before launch.

Ask questions only when the answer changes product behavior, cost, permissions, or external side effects. Otherwise investigate and make the narrowest safe assumption explicit.

## Output

Return a concise launch packet: goal, scope, non-goals, evidence inspected, risks, decisions, acceptance checks, and stop conditions. Use it as the input to `gap-analysis` or `implement`.
