---
name: efficient-fable
description: Use Claude Fable efficiently on codebase-heavy work by reserving it for judgment and synthesis while cheaper agents handle bounded research, coding, and testing. Use when a large task benefits from delegation but still needs a strong final decision-maker.
---

# Efficient Fable

Use Fable for decisions; delegate repetitive evidence gathering.

## Pattern

1. Identify the expensive surface: broad repository scans, lengthy logs, repetitive edits, or test runs.
2. Split independent slices into explicit, bounded subagent assignments.
3. Require concise evidence: file references, commands, diffs, failures, and uncertainty.
4. Have Fable resolve contradictions, choose the path, coordinate shared changes, and review the final result.
5. Reopen important evidence before making high-impact claims or declaring success.

Keep tightly coupled work with the orchestrator. Do not delegate product judgment merely because a task is large.
