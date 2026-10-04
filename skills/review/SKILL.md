---
name: skill-definition-review
description: Review skill definitions as complete behavioral specifications, using related repository structure, skills, governing instructions, and setup artifacts when needed to judge activation, responsibility boundaries, phase scope, recurring cost, and whether the target skill expresses its intended behavior with a minimal rule set.
---

# Skill Definition Review

Use this skill when reviewing a `SKILL.md` file or an equivalent skill definition.

Treat the changed skill as one complete behavioral specification and keep it as the review target.
Inspect related skills, repository structure, governing instructions, and setup artifacts when they are needed to judge that skill's activation, responsibility boundary, phase ownership, or recurring cost.
Use the diff to understand the intended change, then judge the resulting full definition.

## Check activation

Review the frontmatter description together with the opening usage guidance.
Confirm that they express the skill's purpose, applicable situations, and important distinctions introduced by the body.

## Check the rule system

Read all rules together before reporting findings.
Check the applicability of each rule, especially distinctions between different modes or phases of work.
Check for duplicated behavior, conflicting instructions, uncovered cases, and broad rules that override narrower intended behavior.
Prefer direct positive rules and compact closed boundaries.

## Check responsibility boundaries

Confirm that the skill governs one coherent concern.
Assign surrounding workflow, repository, implementation, and process details to the skills that own those responsibilities.
Prefer the smallest rule set that preserves the intended behavior.
Confirm that materially different phases have separate owners when their inputs, decisions, or outputs differ.

## Check recurring execution cost

Identify repository discovery, classification, or configuration repeated during normal use.
Prefer installation-time or introduction-time setup for stable repeated work when the prepared result makes later runs lighter.
Keep dynamic decisions in the phase where current state matters.
Confirm that setup artifacts provide recurring value proportional to their maintenance cost.

## Check the change across the whole skill

Identify the intended behavioral change from the request or review context.
Trace that change through the frontmatter, usage guidance, relevant rules, and closing responsibility statement.
Check existing text whose meaning changes because of the new behavior.

## Complete the review

Inspect the full effective skill definition before reporting findings.
Report findings that require a change together after the review pass is complete.
Treat a finding as requiring change when it exposes a material defect in intended behavior, coverage, consistency, recurring cost, or responsibility boundary.
Treat further precision that preserves the intended behavior as optional refinement.
After reported findings are addressed, reassess the resulting definition against the same intended behavior and review criteria, and conclude the review when no material defect remains.
