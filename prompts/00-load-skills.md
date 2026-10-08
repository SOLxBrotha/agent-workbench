# Summarize and load applicable skills

Do not change runtime code, dependencies, tests, infrastructure, or product behavior.

Read `https://github.com/SOLxBrotha/agent-workbench`, including its `README.md`, `AGENTS.md`, and every `skills/*/SKILL.md`. Treat that repository as a generic skill source, not as product context. Read the target repository's current instructions, PRDs, installed skills, provider contracts, active work, worktrees, and Git state.

First, give the user a concise plain-language summary of the workflow and each available skill. Then state which skills apply and why, which do not apply and why, and install only the applicable skills.

Use this applicability rule:

- owned software work: `workbench-controlled-work` and `workbench-minimal-build`;
- external API, SDK, platform, or managed-service work: also `workbench-provider-boundary`;
- a standing repository/release owner: also `workbench-devops`;
- multi-capability coordination: also `workbench-integration-parent`;
- bounded capability ownership: also `workbench-feature-parent`;
- delegated narrow tasks: also `workbench-executor`.

Do not install role skills for roles the target workflow does not use.

The installation must:

- preserve current valid product, provider, design, security, commercial, legal, and operational requirements;
- use the target repository's established skills location, or `.agents/skills/` when no convention exists;
- keep one canonical copy of each selected skill;
- add concise routing references to the existing `AGENTS.md` without replacing current valid rules;
- copy only the selected generic `skills/*/SKILL.md` packages from Agent Workbench;
- copy no product-specific names, paths, policy, secrets, or private material from any other project;
- create no runtime, dependency, service, automation, archive, or duplicate report;
- leave runtime code, dependencies, tests, infrastructure, configuration, UI, and product behavior unchanged.

The user's request to load applicable skills authorizes these documentation-only installation changes. Stop before editing if active work has unknown ownership, instructions conflict, or the target would fall outside this scope.

Validate installed skill names, directory-name parity, frontmatter, relative links, duplicate copies, routing references, prohibited private/product context, and the complete diff. Return the summary, selected and skipped skills with reasons, exact changed files, checks, and exactly one next action. Stop after installation.
