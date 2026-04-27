---
name: code-review
description: Use after a milestone or code change to review correctness, hidden-test risks, architecture drift, missing tests, and unclear assumptions before moving on.
---

# Code Review Skill

Use this skill after finishing a milestone or meaningful code change. The goal is to catch conceptual and behavioral problems before the next implementation step.

## Instructions

1. Read the relevant roadmap entry in `docs/milestone-roadmap.md`.
2. Read the current state in `PROJECT_STATE.md`.
3. Inspect the files changed for the current milestone.
4. Compare the implementation against the relevant `SPEC.md` section.
5. Check correctness rules, invariants, edge cases, and hidden-test risks.
6. Check whether the change silently altered architecture or public behavior.
7. Check whether the tests actually prove the intended behavior.
8. Identify missing tests or unclear assumptions.
9. Recommend minimal fixes before moving on.

Do not implement the next milestone during review. If a fix is needed, keep it scoped to the reviewed milestone.

## Review Priorities

Prioritize findings in this order:

1. Correctness bugs.
2. Spec violations.
3. Hidden-test and edge-case risks.
4. Missing or weak tests.
5. Architecture drift or unclear design decisions.
6. Learning gaps and concepts that should be reviewed.
7. Style issues only when they affect clarity, maintainability, or tests.

## Output Format

### Findings

List issues by severity with file and line references when possible.

### Spec Alignment

### Invariant Check

### Test Coverage

### Architecture Check

### Hidden-Test Risks

### Learning Notes

### Recommended Fixes

### Ready To Continue?
