---
name: teach-while-building
description: Use when modifying code in a learning project and the user wants theory, implementation, invariants, tests, and examples explained together.
---

# Teach While Building Skill

Use this skill when code changes should be paired with theory, examples, invariants, and tests.

## Instructions

When modifying code, explain:

- What problem is being solved.
- What concept this implements.
- What state changes.
- What invariant must hold.
- What can go wrong.
- How the test verifies correctness.
- How the code maps to the spec.

Use concrete examples. Avoid vague summaries such as "this handles the logic" or "this makes it work." Name the exact state, rule, edge case, or failure mode involved.

## Teaching Standard

For each important change, connect:

- Spec requirement to observable behavior.
- Observable behavior to implementation mechanism.
- Implementation mechanism to correctness rule.
- Correctness rule to test strategy.
- Failed behavior to the likely conceptual misunderstanding.

Prefer small examples that can be traced by hand.
