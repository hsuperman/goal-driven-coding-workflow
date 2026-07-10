---
name: calling-claude
description: Run Claude CLI non-interactively for focused research, design judgment, or delegated implementation. Use when the workflow calls for Claude or Fable and the local environment is authenticated.
---

# Calling Claude

Run Claude in print mode with a scoped prompt:

```bash
claude -p "<prompt>" --model <model>
```

Check authentication before treating a failed call as a task failure. Include the repository path, exact objective, scope, evidence expected, checks to run, and stop conditions. Ask the agent to report uncertainty rather than inventing missing product decisions.

Use Fable for architecture, synthesis, and final judgment; use less-expensive agents for bounded scans, mechanical edits, and test execution.
