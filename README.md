# Skill Development

A lightweight workflow for designing, implementing, and reviewing skill repositories.

Each skill owns one phase. Later phases use the settled output of earlier phases as input.

## Skills

- `skill-development-planning`: decide whether an existing skill is sufficient, define the smallest repository and skill boundaries, and choose setup that reduces recurring work.
- `skill-development-implementation`: implement the settled skill structure with compact, direct instructions and any selected setup.
- `skill-definition-review`: review the resulting skill definitions as complete behavioral specifications.

## When to use

- Use `skill-development-planning` when creating or restructuring a skill repository before its skill boundaries, responsibilities, README contract, and setup are settled.
- Use `skill-development-implementation` after those decisions are settled and need to be reflected in the repository.
- Use `skill-definition-review` when reviewing a `SKILL.md` or equivalent definition and its supporting public README contract.

## Installation

Install the skill directories you need from `skills/` into the skill location used by your agent or skill loader.
For loaders that use one skill per directory, install `skills/planning`, `skills/implementation`, and `skills/review` as separate skill directories.
Install all three when using the complete planning, implementation, and review workflow.

## Design principles

Prefer the smallest set of skills that expresses the workflow clearly.
Split skills when work phases have materially different inputs, decisions, or outputs.
Prefer direct positive rules that state the desired action or boundary.
Move stable repeated discovery into installation-time setup when that makes normal skill use lighter.
Use existing skills for concerns they already own.
Keep repository-specific setup proportional to the recurring work it removes.
Preserve stable public context in the repository README: the core idea, each skill's responsibility, when each skill should be activated, how to install the published skills, and ownership of adjacent concerns that are easy to confuse with them.
Express responsibility boundaries through affirmative ownership statements.
Name the owning skill when one is already selected; otherwise assign the concern to a separate skill responsibility.
Keep operational behavior in `SKILL.md`.

## Repository shape

This repository uses:

```text
skills/
├── planning/
│   └── SKILL.md
├── implementation/
│   └── SKILL.md
└── review/
    └── SKILL.md
```
