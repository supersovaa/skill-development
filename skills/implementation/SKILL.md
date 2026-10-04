---
name: skill-development-implementation
description: Implement a settled skill-repository plan with minimal files, phase-focused skill definitions, direct positive rules, and setup that keeps normal skill use lightweight.
---

# Skill Development Implementation

Use this skill after the skill-repository structure and responsibility boundaries are settled.

## Follow the settled boundaries

Read the selected development plan from the current work context or the durable planning artifact selected by the surrounding workflow.
Read the current repository state.
Implement the planned skill set and supporting files.
Keep each skill focused on its assigned phase or coherent responsibility.
Preserve existing public skill names when the plan selects compatibility.

## Keep definitions compact

Include behavior that materially affects execution.
Reference shared or existing skills when they already own a rule.
Prefer one direct rule over several equivalent clarifications.
Represent current requirements and current workflow rather than speculative future cases.

## Write positive operational guidance

State the expected action or boundary directly.
Prefer affirmative forms such as "use only", "choose", "keep", "require", and "prefer".
Use negative wording when absence, prohibition, or unsupported behavior is itself the operative fact.

## Implement setup where planned

Create installation-time or repository-introduction setup when the plan assigns stable repeated work there.
Persist only information that remains useful across normal executions.
Make normal skill execution consume the prepared result directly.
Keep setup small enough that maintaining it remains cheaper than repeating the work it replaces.

## Apply referenced skills

Apply reusable skills selected by the development plan for concerns they own.
Apply `scope-aligned-naming` when repository or path naming is part of the implementation.
Maintain a concise README when the repository contains multiple skills or setup steps.

## Validate the result

Confirm that:

- every planned responsibility has one clear owner;
- phase boundaries remain explicit;
- normal execution carries only the context it needs;
- setup removes recurring work where intended;
- each skill definition uses the smallest rule set that preserves behavior;
- repository documentation matches the implemented structure.

Leave the resulting skill definitions ready for independent review by `skill-definition-review`.

This skill owns implementation of the settled skill-repository plan.
Planning belongs to `skill-development-planning`.
Review belongs to `skill-definition-review`.
