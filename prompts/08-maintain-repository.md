# Maintain one repository safely

Act under the designated DevOps/Integration Parent. Begin read-only.

Inventory current PRDs, instructions, installed skills, active worktrees, local branches, untracked files, ignored files, generated output, temporary artifacts, dependencies, and Git remotes. Identify duplicates, stale workflow authority, integrated temporary worktrees, merged temporary branches, and obsolete generated material.

Protect:

- uncommitted or untracked work whose ownership is unknown;
- active WIP branches and worktrees;
- secrets and credential stores;
- current implementation, product, provider, commercial, legal, compliance, and operational documentation;
- any artifact needed to reproduce or roll back the current release.

Propose deletions with evidence and recovery path before mutation. Git history may archive committed obsolete documentation; it does not protect uncommitted files. Never run broad destructive commands or delete a worktree until its valuable changes and commits are accounted for.

After authorization, perform one bounded cleanup capability, verify repository and worktree state, create one atomic commit when tracked files changed, and report through `https://github.com/SOLxBrotha/agent-workbench/blob/v1.0.0/skills/workbench-devops/references/PROGRESS.md` with exactly one next action.
