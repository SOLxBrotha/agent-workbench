# Summarize and load applicable skills

Do not change runtime code, dependencies, tests, infrastructure, or product behavior.

Read `https://github.com/SOLxBrotha/agent-workbench`, including its `README.md`, `AGENTS.md`, and every `skills/*/SKILL.md`. Read the target repository's current instructions, PRDs, installed skills, provider contracts, active work, worktrees, and Git state.

First, give the user a concise plain-language summary of the workflow and each available skill. Then select and install only the skills that apply to the target repository and current work.

The installation must:

- preserve current valid product, provider, design, security, commercial, legal, and operational requirements;
- use the target repository's established skills location, or `.agents/skills/` when none exists;
- keep one canonical copy of each selected skill;
- add concise routing references to the existing `AGENTS.md` without replacing current valid rules;
- copy no product-specific paths, policy, secrets, or private material from another project;
- create no runtime, dependency, service, automation, archive, or duplicate report;
- leave runtime code, dependencies, tests, infrastructure, configuration, UI, and product behavior unchanged.

The user's request to load applicable skills authorizes these documentation-only installation changes. Stop before editing if active work has unknown ownership, instructions conflict, or the target would fall outside this scope.

Validate installed skill names, frontmatter, links, duplicate copies, and the complete diff. Return the summary, selected and skipped skills with reasons, exact changed files, checks, and exactly one next action. Stop after installation.
