# Skill Development

A lightweight workflow for designing, implementing, and reviewing skill repositories.

Each skill owns one phase. Later phases use the settled output of earlier phases as input.

## Skills

- `skill-development-planning`: decide whether an existing skill is sufficient, define the smallest repository and skill boundaries, and choose setup that reduces recurring work.
- `skill-development-implementation`: implement the settled skill structure with compact, direct instructions and any selected setup.
- `skill-definition-review`: review the resulting skill definitions as complete behavioral specifications.

## Design principles

Prefer the smallest set of skills that expresses the workflow clearly.
Split skills when work phases have materially different inputs, decisions, or outputs.
Prefer direct positive rules that state the desired action or boundary.
Move stable repeated discovery into installation-time setup when that makes normal skill use lighter.
Use existing skills for concerns they already own.
Keep repository-specific setup proportional to the recurring work it removes.
Preserve stable design context in the repository README, especially the core idea and responsibility boundaries that future changes need to keep intact.
Keep operational behavior in `SKILL.md` instead of duplicating its rule set in the README.

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
