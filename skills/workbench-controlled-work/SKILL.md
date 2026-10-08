---
name: workbench-controlled-work
description: Mandatory for implementation and release execution. Governs fixed points, role ownership, independent parallelism, atomic commits, integration, regressions, temporary worktrees, PRD matrices, and handoff.
---

# Controlled Work

For solo work, one owner may carry the capability from fixed base through verification and atomic commit without loading role skills. For coordinated work, one repository/integration owner maintains repository truth and release evidence, one capability owner owns each bounded capability, and task workers receive narrower assignments. Parallelize independent mutable scopes; serialize shared files, state, and provider mutation paths.

Apply `workbench-minimal-build` to project-owned implementation and `workbench-provider-boundary` whenever the capability crosses an external provider boundary. Role skills change responsibility, not implementation authority.

Every capability starts with a recorded base SHA, PRD item, owner, outcome, mandatory skills, allowed paths, protected paths, dependencies, expected change, acceptance gate, and stop conditions.

One verified capability equals one atomic commit. Inspect every changed file and hunk, stage explicit files or hunks, remove unrelated changes, run existing relevant checks, and verify the outcome. Hand Integration commit SHAs and evidence, never an uncontrolled working tree.

For a regression, stop affected feature work and compare the newest capability commit with the immediately preceding known-good head. Fix or revert the responsible capability only. Do not launch a broad audit without evidence.

Create a worktree only when concurrent mutable work needs isolation. After verified integration, confirm no valuable uncommitted state, remove the temporary worktree, and prune metadata. Git commits are continuity and history. Apply `workbench-devops`, `workbench-integration-parent`, `workbench-feature-parent`, and `workbench-executor` only when those roles exist.

Every product or process uses one current PRD with a fixed, dependency-ordered matrix. Mark `✅ PASS` only for observed completion. Close with provider-boundary audit, minimal-build audit, and successful product/process checks.
