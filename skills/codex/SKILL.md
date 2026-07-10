---
name: codex
description: Run OpenAI Codex CLI for bounded implementation, analysis, or review work, including resumable sessions and independent second opinions. Use when delegating a task to Codex or when a fresh technical perspective would reduce risk.
---

# Codex

Use `codex exec` for automation and `codex exec resume` to retain context:

```bash
codex exec -m <model> -c 'model_reasoning_effort="high"' "<prompt>"
codex exec resume <session-id> "<follow-up prompt>"
```

Record the session ID from the first response and resume it for corrective feedback, follow-up tests, or implementation steps. Write prompts as self-contained work orders: objective, scope, relevant files, constraints, acceptance checks, and stop conditions.

For review, use a read-only session when possible. Give Codex the artifact to assess and ask for concrete risks, missing cases, incorrect assumptions, and the smallest correction.

Keep review distinct from implementation:

1. Ask for an independent assessment without supplying your conclusion.
2. Verify important findings against the repository.
3. Decide which findings change the plan.
4. Feed only concrete corrective feedback into the implementation session.

Use this in `gap-analysis` for the overall queue and in `orchestrating-subtasks` for high-risk changes. Use a trusted repository and environment for any sandbox-bypass or auto-approval option, and never put credentials or private source material in a prompt or log.
