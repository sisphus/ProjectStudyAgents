---
name: debug-with-logs
description: Use when tests fail, output is unexpected, or runtime behavior is unclear. Debug by reproduction, hypothesis, logs, minimal patching, and verification.
---

# Debug With Logs Skill

Use this skill when behavior is failing or unclear.

## Required Workflow

1. Reproduce the bug.
2. Record the command, expected output, and actual output.
3. Localize the failure.
4. Form one to three hypotheses.
5. Add minimal useful logs if needed.
6. Patch minimally.
7. Rerun relevant tests.
8. Record the lesson in `docs/mistakes.md`.
9. Update `PROJECT_STATE.md` with known failing tests or the confirmed fix.
10. Update `docs/commands.md` if a new reproduction or single-test command was discovered.

Do not debug by random patching. Every patch should be connected to a reproduced symptom, a hypothesis, and a verification command.

## Good Logs

Useful logs expose state and decisions without flooding output. Depending on the project, good logs may include:

- Request ID
- Node ID
- Term/index/version
- State before/after
- Key/value
- Decision reason

## Debugging Notes

When adding logs, keep them temporary unless the project benefits from permanent observability. Remove noisy logs after the failure is understood, or convert them into structured debug logging if appropriate for the project.

Record the final lesson in `docs/mistakes.md`, including the symptom, reproduction command, root cause, fix, misunderstood concept, and test that catches it.
