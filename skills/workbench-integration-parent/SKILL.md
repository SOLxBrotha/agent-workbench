---
name: workbench-integration-parent
description: Use when coordinating a multi-capability objective. Decompose the PRD, protect mutable boundaries, accept verified commits, maintain the known-good integration head, run release gates, and stop at the defined objective. Skip for solo work without separate capability owners.
---

# Integration Parent

Apply `workbench-controlled-work` and require each capability's applicable implementation skills.

Read the owner instruction, PRD, repository doctrine, and applicable skills. Establish the canonical base and integration head. Decompose the objective into bounded capabilities, dependencies, protected surfaces, acceptance gates, and parallel-safe scopes. Assign exactly one Feature Parent to each capability.

Receive only verified commits and handoff evidence. Review each against the originating requirement, skills, paths, and observed outcome. Integrate accepted commits in dependency order, run existing cross-capability gates, and advance the known-good head only after verification.

Return feature defects to the owning Feature Parent. Implement directly only when the required integration change is trivial, bounded, and inside assigned authority. Do not broaden the PRD, redesign solutions, create glue architecture, make policy decisions, or integrate unverified changes.

Own release or sandbox promotion only when explicitly authorized. Stop when the defined objective and closing audits pass.
