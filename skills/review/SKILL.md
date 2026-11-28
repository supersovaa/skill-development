---
name: skill-definition-review
description: Use when reviewing a skill definition or its published activation and installation guidance.
---

# Skill Definition Review

Review the resulting `SKILL.md` or equivalent as a complete behavioral specification. When reviewing a change, use its diff to identify the intended behavior.

Inspect related skills, the repository layout, governing instructions, the public README, and setup artifacts as needed to judge activation, responsibility and phase boundaries, installation, or recurring cost.

## Check activation

Treat the frontmatter description and opening usage guidance as activation-routing surfaces.
Confirm that they identify the skill from externally recognizable task intent and responsibility boundaries.
Treat an activation condition as too narrow when it requires a prerequisite, internal decision, execution step, or check that the skill itself can perform after activation and that condition is not needed to select a different owner.
Check a normal request for the work type that does not mention the issue the skill can discover. It should select the skill. Then check cases with and without that issue: only the applicable procedure should run. Keep conditions that distinguish different owners at the entry.

## Check the published README

When the reviewed skill is published from a repository, confirm that the repository README states when each published skill should be activated.
Confirm that the README explains how to install the published skill set.
Confirm that README activation guidance uses the same responsibility boundary as the corresponding frontmatter description and opening usage guidance.
Confirm that the activation and installation guidance matches the skill definitions, repository layout, and target skill system.
Keep detailed operational behavior in the skill definitions rather than duplicating it into the README.

## Check the rule system

Read all rules together before reporting findings.
Check the applicability of each rule, especially distinctions between different modes or phases of work.
Check for duplicated behavior, conflicting instructions, uncovered cases, and broad rules that override narrower intended behavior.
Prefer direct positive rules and compact closed boundaries.

## Challenge exceptions

For every exception, require a concrete current requirement or external constraint and evidence that refining the rule's scope or expressing a narrower general rule does not resolve the case.
Treat an exception without that support as a defect and prefer removing it or replacing it with a coherent general rule.
Accept an exception only for cases covered by the same supporting requirement or constraint.
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
Check whether affected existing rules were replaced, consolidated, or removed when the change makes them outdated, overlapping, or redundant.
Confirm that each added rule expresses an independent requirement that cannot be stated more directly by revising an existing rule.

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
