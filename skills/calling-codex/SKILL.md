---
name: calling-codex
description: Run OpenAI Codex CLI non-interactively for a one-shot task or a resumable multi-turn coding session. Use when delegating implementation, analysis, or review work to Codex.
---

# Calling Codex

Use `codex exec` for automation and `codex exec resume` to retain context.

```bash
codex exec -m <model> -c 'model_reasoning_effort="high"' "<prompt>"
codex exec resume <session-id> "<follow-up prompt>"
```

Record the session ID from the first response and resume it for corrective feedback, follow-up tests, or implementation steps. Write prompts as self-contained work orders: objective, scope, relevant files, constraints, acceptance checks, and stop conditions.

Use any sandbox-bypass or auto-approval option only in a repository and environment the user explicitly trusts. Never put credentials or private source material in a prompt or log.
