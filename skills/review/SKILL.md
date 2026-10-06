---
name: skill-definition-review
description: Review skill definitions as complete behavioral specifications, correct clear local defects directly, and block only when a materially mistaken premise is being compounded across the skill or its surrounding workflow.
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

## Challenge exceptions

For every exception, identify the concrete current requirement or external constraint that requires it.
Treat an exception without such support as a defect and prefer removing it or replacing it with a coherent general rule.
Check whether refining the rule's scope or expressing a narrower general rule eliminates the exception.
Do not accept convenience, hypothetical future compatibility, or isolated implementation ease as justification.
Do not infer additional exception cases from an existing exception.
When exceptions cluster, treat that as evidence that the governing rule or responsibility boundary may be wrong and escalate when correction requires a design decision.

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

## Correct clear local defects

Treat a defect as a local correction when the intended correction is uniquely determined by the existing purpose, rules, and referenced skills and requires no new design, responsibility, compatibility, or policy decision.
When the current workflow permits modifying the target, apply the local correction directly.
Otherwise, report the exact correction as a non-blocking item.
Continue the review after applying or recording local corrections.
Keep local corrections out of the blocking findings.

## Escalate mistaken premises

Report a blocking finding when the reviewed change appears to build on a materially mistaken premise about the requested behavior, responsibility boundary, governing source, or workflow and continuing from that premise would compound the mistake.

Treat a choice between materially different behaviors or responsibilities as blocking only when that choice exists because the reviewed change is already building on an unresolved or mistaken premise.

Explain the mistaken premise, the resulting direction that becomes unreliable, and the decision needed to resume safely.

## Complete the review

Inspect the full effective skill definition before reporting findings.
Report blocking findings together after the review pass is complete.
Treat further precision that preserves the intended behavior as optional refinement.
After reported findings are addressed, reassess the resulting definition against the same intended behavior and review criteria, and conclude the review when no blocking mistaken premise remains.
