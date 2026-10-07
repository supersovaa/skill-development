---
name: skill-development-implementation
description: Implement a settled skill-repository plan with minimal files, phase-focused skill definitions, README responsibility, activation, and installation context, direct positive rules, and setup that keeps normal skill use lightweight.
---

# Skill Development Implementation

Use this skill when carrying out an already-decided change in a repository that publishes one or more skills.

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

## Avoid unplanned exceptions

Implement settled rules consistently across their stated scope.
Implement an exception only when the settled plan explicitly defines it and ties it to a concrete current requirement or external constraint that cannot be represented by a refined scope or narrower general rule.
Scope every accepted exception exactly to the requirement or constraint that justifies it.
When implementation reveals an unplanned exception or multiple exceptions, return the governing rule or responsibility boundary to planning instead of deciding the exception locally.

## Implement setup where planned

Create installation-time or repository-introduction setup when the plan assigns stable repeated work there.
Persist only information that remains useful across normal executions.
Make normal skill execution consume the prepared result directly.
Keep setup small enough that maintaining it remains cheaper than repeating the work it replaces.

## Document stable design context

Create or maintain a concise repository README for a published skill repository.
Record the core idea that the repository or skill exists to express.
Record what each skill is responsible for.
Record when each published skill should be activated from externally recognizable task intent and responsibility boundaries.
Use the same activation boundary in the repository README, the skill frontmatter description, and the opening usage guidance.
Keep body-specific prerequisites, internal decision criteria, execution steps, and post-activation checks in `SKILL.md` unless they select a different responsible skill.
Record how to install the published skill set into its target skill system.
For adjacent concerns that need explicit distinction, record their actual owner.
Write responsibility boundaries as affirmative ownership statements.
Name the owning skill when one is already selected; otherwise assign the concern to a separate skill responsibility.
Keep the README at the responsibility and usage-entry level and place executable behavior and detailed operational rules in `SKILL.md`.

## Apply referenced skills

Apply reusable skills selected by the development plan for concerns they own.
Apply `scope-aligned-naming` to names within that skill's defined scope.

## Validate the result

Confirm that:

- every planned responsibility has one clear owner;
- adjacent concerns that need distinction have an explicit owner;
- phase boundaries remain explicit;
- normal execution carries only the context it needs;
- setup removes recurring work where intended;
- each skill definition uses the smallest rule set that preserves behavior;
- the README records the settled core idea and current responsibility allocation;
- the README states when every published skill should be activated;
- the README, frontmatter description, and opening usage guidance use the same activation boundary;
- each activation condition is no narrower than required to select the correct responsibility and does not inherit internal body conditions;
- the README provides an installation method that matches the implemented repository layout and target skill system;
- repository documentation matches the implemented structure.

Leave the resulting skill definitions ready for independent review by `skill-definition-review`.

This skill owns implementation of the settled skill-repository plan.
Planning belongs to `skill-development-planning`.
Review belongs to `skill-definition-review`.
