---
name: skill-development-planning
description: Plan a lightweight skill repository by checking existing skills first, defining coherent phase boundaries, choosing the minimum supporting structure, preserving responsibility, activation, and installation context in the README, and moving repeated stable work into setup when that reduces normal-use cost.
---

# Skill Development Planning

Use this skill when creating or restructuring a repository that publishes one or more skills.

## Start from existing capabilities

Inspect relevant existing skills before defining new ones.
Reuse an existing skill when it already provides the required behavior.
Extend an existing skill when the new behavior belongs to the same coherent responsibility.
Create a new skill when the required behavior has its own responsibility or execution phase.

## Define phase boundaries

Treat each materially different work phase as a candidate skill boundary.
Prefer separate skills when phases differ in their required inputs, permitted decisions, persistent outputs, or completion criteria.
Keep one skill when the work forms one coherent operation with the same execution context.

Use the smallest set of skills that preserves those boundaries clearly.

## Keep the repository lightweight

Prefer the minimum files and supporting artifacts required for reliable use.
Apply `scope-aligned-naming` to names within that skill's defined scope.
Reference existing reusable skills instead of copying their rules.

## Preserve stable design context

Identify the core idea that the repository or skill exists to express.
Define what each skill is responsible for.
Define when each published skill should be activated from user-visible situations.
Define the installation method that makes each published skill available to its target system.
Identify adjacent concerns that are easy to confuse with each responsibility and assign each concern to its actual owner.
Describe the current responsibility allocation with affirmative ownership statements.
Name the owning skill when one is already selected; otherwise assign the concern to a separate skill responsibility.
Plan a concise repository README that records this design context, activation guidance, and installation method.
Keep executable behavior and detailed operational rules in `SKILL.md`.

## Design setup around recurring cost

Identify discovery, classification, or configuration that would otherwise repeat during normal skill use.
Move stable repeated work into installation-time or repository-introduction setup when the stored result makes later runs simpler or cheaper.
Keep dynamic information in normal execution when current state materially affects the decision.
Create setup artifacts only when their recurring value exceeds their maintenance cost.

## Prefer direct positive rules

Write rules as the action, preference, condition, or closed boundary the agent should follow.
Prefer forms such as "use", "choose", "keep", "require", and "use only".
Use a negative statement when the negation itself carries an independent semantic constraint.

## Resist exceptions

Prefer rules that apply consistently across their stated scope.
Justify an exception only with a concrete current requirement or external constraint that cannot be represented by refining the rule's scope or by a narrower general rule.
Make every accepted exception explicit and scope it exactly to the requirement or constraint that justifies it.
When multiple exceptions appear necessary, redesign the governing rule or responsibility boundary instead of accumulating them.

## Produce the development plan

Define:

- the skills to create, retain, move, or revise;
- the core idea and responsibility of each skill;
- the ownership of adjacent concerns that need explicit distinction;
- the phase relationship between skills;
- the minimum repository structure;
- the stable design context to preserve in the repository README;
- the README activation guidance for each published skill;
- the README installation method for the published skill set;
- any installation-time or introduction-time setup;
- existing skills that remain dependencies or review tools;
- compatibility decisions for existing skill names and entry points.

Record implementation mechanics only when they are already settled constraints.

## Hand off the plan

Return the development plan in the current work context for immediate implementation.
When the surrounding workflow requires durable planning state, persist the plan using that workflow's established plan location and format.
Make the selected plan identifiable to the implementation phase.

This skill owns skill-repository planning.
Implementation belongs to `skill-development-implementation`.
