# Skill Development

A lightweight workflow for designing, implementing, and reviewing skill repositories.

Each skill owns one phase. Later phases use the settled output of earlier phases as input.

## Skills

- `skill-development-planning`: decide whether an existing skill is sufficient, define the smallest repository and skill boundaries, and choose setup that reduces recurring work.
- `skill-development-implementation`: implement the settled skill structure with compact, direct instructions and any selected setup.
- `skill-definition-review`: review the resulting skill definitions as complete behavioral specifications.

## When to use

- Use `skill-development-planning` when deciding how a skill repository should be structured, divided, documented, or set up.
- Use `skill-development-implementation` when carrying out an already-decided change in a skill repository.
- Use `skill-definition-review` when reviewing a skill definition, including the README guidance that publishes its activation and installation.

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
Base activation guidance on externally recognizable task intent and responsibility boundaries.
Use the same activation boundary in the README, the skill frontmatter description, and the opening usage guidance.
Keep body-specific prerequisites, internal decision criteria, execution steps, and post-activation checks in `SKILL.md` unless one of them is itself the boundary between skills.
Prefer activating the owning skill and letting it evaluate its internal conditions over encoding those conditions into activation routing.
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
