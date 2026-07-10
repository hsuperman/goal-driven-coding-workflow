# Goal-Driven Coding Workflow

A small, portable skill pack for moving from a product goal to verified implementation.

It is intentionally generic: no application code, customer data, internal URLs, project history, or company-specific operating rules are included.

## The workflow

1. `/authoring-goal-docs` — research the codebase and write a durable product goal.
2. `/grill-for-unknowns` — challenge assumptions, dependencies, and proof before planning.
3. `/gap-analysis` — turn the agreed goal into a prioritized task queue.
4. `/gap-close` — execute the approved queue through `/orchestrating-subtasks`.

Supporting skills:

- `/efficient-fable` — reserve Fable for judgment and delegate bounded work.
- `/calling-claude` — run Claude/Fable non-interactively when available.
- `/codex` — run resumable Codex CLI sessions and request an independent review or second opinion.
- `/implement` — apply the shared preflight and verification loop.

## Install

Copy the skills you want into Codex's skills directory:

```bash
git clone https://github.com/hsuperman/goal-driven-coding-workflow.git
mkdir -p ~/.codex/skills
cp -R goal-driven-coding-workflow/skills/<skill-name> ~/.codex/skills/
```

Repeat the copy command for each skill you want. Start with the four workflow skills and add the supporting skills required by your chosen model setup.

## Requirements

- A Codex-compatible skill host.
- Git and a local repository to inspect.
- Codex CLI for `/codex`.
- Claude CLI and authentication only if using `/calling-claude` or `/efficient-fable` with Claude/Fable.

The pack describes a workflow; it does not install models, authenticate providers, or make deployments automatic. Review each skill and adapt it to your own repository's safety rules before giving agents write access.

## Attribution

This is a small, rewritten workflow pack. It does not contain application code or a verbatim copy of any upstream skill.

- `/grill-for-unknowns` is adapted from Nico Bailon's public [`grill-for-unknowns` repository](https://github.com/nicobailon/grill-for-unknowns). That project credits Matt Pocock's [`grill-with-docs`](https://github.com/mattpocock/skills/blob/main/skills/engineering/grill-with-docs/SKILL.md), [`grilling`](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md), and [`domain-modeling`](https://github.com/mattpocock/skills/tree/main/skills/engineering/domain-modeling), together with Thariq's [“A Field Guide to Fable: Finding Your Unknowns”](https://x.com/trq212/status/2073100352921215386).
- `/codex` is a compact adaptation of the public [`codex` skill from gstack](https://github.com/garrytan/gstack/blob/main/codex/SKILL.md), by Garry Tan. The gstack project is MIT licensed; this pack does not include its runtime, telemetry, or other gstack files.
- `/efficient-fable`, `/calling-claude`, `/implement`, and the goal/gap/orchestration skills are local workflow guidance written for this pack. No gstack provenance was found for them.

The pack is not affiliated with gstack, Matt Pocock, Thariq, Anthropic, or OpenAI.
