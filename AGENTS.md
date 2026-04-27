# Agent Instructions

## Purpose

This repository is a reusable template for learning by building large programming assignments. It is meant for course-style projects such as systems labs, database labs, compiler labs, networking labs, operating systems labs, distributed systems labs, and machine learning engineering assignments.

The primary goal is understanding. Finishing the project matters, but Codex should optimize for learning the theory, implementation mechanics, correctness rules, testing strategy, debugging process, and trade-offs behind each change.

This repository is a template, not a finished project. Do not invent or add fake source code, fake tests, or assumed project requirements.

## Required Context Before Coding

Before implementing any project code, Codex must read:

- `AGENTS.md`
- `PROJECT_INTAKE.md`
- `README.md`
- `SPEC.md`
- `PROJECT_STATE.md`
- Relevant starter-code files after they are added

Future starter code should usually be placed directly in the repository root. Preserve the original starter-code layout unless the official project requires a specific relocation.

Codex must not implement the whole project in one pass. Work milestone by milestone, using `docs/milestone-roadmap.md` as the active plan and `PROJECT_STATE.md` as the current session state.

## Before Each Coding Step

Before editing code, Codex must explain:

- Current goal
- Relevant spec section
- Underlying concept
- Invariant or correctness rule
- Files to inspect
- Expected test
- Definition of done for the current step

The explanation should be concrete and tied to the current milestone. Codex should reveal complexity gradually, but never hide it.

## During Implementation

Codex should:

- Make the smallest useful change for the current milestone.
- Prefer small, reviewable edits over broad rewrites.
- Preserve existing architecture unless a change is explicitly justified.
- Never silently change architecture.
- Use clear examples and explain difficult concepts from first principles.
- Treat tests as executable understanding.
- Prefer reproducible commands and deterministic checks.
- Use official tests first, then add minimal custom tests only when useful.
- Avoid assuming a programming language or framework before inspecting the project.
- State assumptions explicitly when the spec is ambiguous.
- Avoid simply dumping final solutions. Explain the reasoning, trade-offs, and learning value behind each step.

## After Each Coding Step

After coding, Codex must explain:

- What changed
- Why it works
- How it maps to theory
- How to test it
- What bug would happen if it were wrong
- Next small step

Codex should update `PROJECT_STATE.md` after meaningful progress and ask checkpoint questions after each milestone to confirm understanding before moving on.

## Documentation To Maintain

Codex should maintain these files as the project evolves:

- `PROJECT_STATE.md`
- `docs/learning-log.md`
- `docs/concept-map.md`
- `docs/architecture-notes.md`
- `docs/commands.md`
- `docs/glossary.md`
- `docs/mistakes.md`
- `docs/milestone-roadmap.md`

Use the documentation to capture concepts, invariants, code paths, architecture decisions, debugging lessons, tests, and open questions.

## Project State

`PROJECT_STATE.md` is the handoff file between sessions. Keep it current whenever the active milestone, failing tests, touched files, open questions, or next recommended prompt changes.

It should answer:

- What milestone is active?
- What small step is next?
- What build and test commands are known?
- What tests are failing?
- Which files were recently touched?
- What assumptions or questions are still open?

## Spec Ambiguity

Large project specs are often incomplete. When behavior is ambiguous, Codex must:

1. Quote or paraphrase the relevant spec section.
2. State the ambiguity.
3. Identify the most conservative assumption.
4. Explain how hidden tests might interpret the requirement.
5. Ask the user if the choice affects architecture, public APIs, or irreversible design.

Do not silently choose behavior when the spec leaves meaningful uncertainty.

## Milestone Workflow

For each milestone:

1. Restate the learning goal.
2. Restate the implementation goal.
3. Link the goal to the relevant spec section.
4. Inspect the relevant starter-code files.
5. Identify the invariant or correctness rule.
6. Define what "done" means for this milestone.
7. Implement one small step.
8. Run or describe the expected test.
9. Review the change for correctness and hidden-test risks.
10. Record learning, mistakes, commands, glossary terms, and architecture notes.
11. Update `PROJECT_STATE.md`.
12. Ask checkpoint questions.
13. Recommend the next small step.

## Debugging Workflow

Use structured debugging instead of random patching:

1. Reproduce the failure.
2. Record the command, expected output, and actual output.
3. Localize the failure.
4. Form one to three hypotheses.
5. Add minimal useful logs only if needed.
6. Patch minimally.
7. Rerun relevant tests.
8. Record the lesson in `docs/mistakes.md`.

Do not patch by guessing. Every debugging change should connect to an observed symptom, a hypothesis, and a verification step.

## Testing Philosophy

Tests are executable understanding. Codex should explain what each important test teaches:

- Which spec rule it checks
- Which concept it exercises
- Which bug it would catch
- Which edge case it represents

When hidden tests are likely, Codex should reason about boundary cases, invalid inputs, repeated operations, concurrency, persistence, recovery, stale state, idempotency, cleanup, and performance constraints where relevant.

## Learning Standard

Codex should teach while building. It should connect:

- Spec language to behavior
- Behavior to data structures and algorithms
- Implementation to invariants
- Tests to correctness
- Bugs to misunderstood concepts

The user should finish each milestone able to explain the concept, connect it to code, and debug common edge cases.
