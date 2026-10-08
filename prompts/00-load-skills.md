# Summarize and load applicable skills

Do not change runtime code, dependencies, tests, infrastructure, or product behavior.

Read the immutable Agent Workbench release at `https://github.com/SOLxBrotha/agent-workbench/tree/v1.0.0`, including its `README.md`, `AGENTS.md`, and every `skills/*/SKILL.md`. Treat it as a generic skill source, not as product context. Read the target repository's current instructions, PRDs, installed skills, provider contracts, active work, worktrees, and Git state.

Keep these actions distinct:

1. **Inspect:** read the source release and target repository without changing files.
2. **Select:** summarize the workflow and every skill, then map skills to the user's stated next task and actual working model.
3. **Install:** copy complete selected skill packages only.
4. **Activate:** add concise routing for selected skills to the target repository's applicable instruction file.

Select against the user's stated next task. If none is stated, use one unambiguous active task and working model already present in the conversation or target repository. If neither exists, complete the summary and recommendation, make no file changes, and ask for that one missing choice.

Use this applicability rule:

- any owned software task: `workbench-controlled-work` and `workbench-minimal-build`;
- external API, SDK, platform, or managed-service work: also `workbench-provider-boundary`;
- a standing repository/release owner: also `workbench-devops`;
- multi-capability coordination: also `workbench-integration-parent`;
- bounded capability ownership: also `workbench-feature-parent`;
- delegated narrow tasks: also `workbench-executor`.

Do not install role skills for roles the target workflow does not use. Every selected role skill requires `workbench-controlled-work`. Install `workbench-provider-boundary` whenever the stated task crosses a provider boundary. Resolve those dependencies before copying files.

The installation must:

- preserve current valid product, provider, design, security, commercial, legal, and operational requirements;
- use the target repository's supported project-local skill location: preserve its established convention, otherwise use `.agents/skills/` for Agent Skills compatible agents or `.claude/skills/` for Claude Code;
- never write to a user-global skill directory unless the user explicitly requests a global installation;
- keep one canonical copy of each selected skill;
- copy the complete selected generic `skills/*/` packages, including their referenced resources;
- use the narrowest applicable existing instruction file; create a concise root `AGENTS.md` only when none exists and the target supports it;
- add routing only for selected skills without replacing current valid rules;
- record source release `v1.0.0` in the routing note;
- copy no product-specific names, paths, policy, secrets, or private material from any other project;
- create no runtime, dependency, service, automation, archive, or duplicate report;
- leave runtime code, dependencies, tests, infrastructure, configuration, UI, and product behavior unchanged.

Before replacing a same-name installed skill, compare it with the source. Leave an identical copy unchanged. If it differs or contains local modifications, stop and show the conflict; do not merge or overwrite authority by assumption.

The user's request to load applicable skills authorizes these documentation-only installation changes. Stop before editing if active work has unknown ownership, instructions conflict, a selected dependency is unavailable, or the target would fall outside this scope.

Validation passes only when selected package directories match their frontmatter names, required frontmatter is present, internal links resolve, selected dependencies are installed, exactly one project-local copy exists, routing names only selected skills and source `v1.0.0`, prohibited private/product context has zero hits, `git diff --check` passes, and the complete diff contains only authorized documentation/skill files.

Return the plain-language summary, selected and skipped skills with reasons, source release, install location, exact changed files, validation results, conflicts or limitations, and exactly one next action. Stop after installation.
