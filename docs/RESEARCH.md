# Research basis and selection decisions

This package was assembled from current first-party guidance, a proven fixed-point delivery workflow, and a bounded review of public agent-workflow repositories. It adopts ideas, not third-party text.

## Primary sources

- [OpenAI: Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) supports concise skills, precise descriptions, progressive disclosure, and removing contradictory or overlapping instructions.
- [OpenAI: Running Codex safely](https://openai.com/index/running-codex-safely/) supports sandboxing, bounded permissions, restricted network access, controlled credentials, and auditability.
- [OpenAI: Harness engineering](https://openai.com/index/harness-engineering/) supports a repository as the system of record, a short map to deeper authority, isolated work, and agent-legible verification.
- [GitHub: Copilot coding agent risks and mitigations](https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations) documents unvalidated-code, prompt-injection, credential, network, and review risks.
- [GitHub secret scanning](https://docs.github.com/en/code-security/concepts/secret-security/secret-scanning) and [push protection](https://docs.github.com/en/code-security/how-tos/secure-your-secrets/prevent-future-leaks) support scanning public history and blocking supported secrets before they land.
- [GitHub secure use of Actions](https://docs.github.com/en/actions/reference/security/secure-use) supports least privilege and pinning third-party actions to immutable commit SHAs. This release adds no Actions workflow, avoiding that supply-chain surface entirely.
- [NIST Secure Software Development Framework](https://csrc.nist.gov/pubs/sp/800/218/final) supports integrating secure practices into the lifecycle, reducing vulnerabilities, limiting impact, and preventing recurrence.
- [Agent Skills specification](https://agentskills.io/specification) defines the portable `SKILL.md` format used here.
- [AGENTS.md](https://agents.md/) defines the open repository-instruction convention used by the pack.

## Public repository survey

### Matt Pocock's `skills`

Reviewed [`mattpocock/skills`](https://github.com/mattpocock/skills) at commit `6fd947921b935b7e1e69293a200400f0fdd5c15f`.

Adopted:

- small, composable skills that leave control with the developer;
- context pointers and progressive disclosure instead of one giant instruction file;
- primary-source research with citations;
- a fixed comparison point for review;
- separate review of requirement fidelity and repository standards;
- narrow end-to-end slices with explicit dependencies;
- reproduce and minimize a defect before changing code.

Not adopted as defaults:

- mandatory new tests or a new TDD framework for every change;
- speculative prefactoring or architecture improvement;
- maximum subagent concurrency;
- a mandatory issue tracker or triage state machine;
- long user-story inventories when a precise current outcome is sufficient.

These omissions preserve the minimum-diff rule and keep the pack usable in existing repositories without installing process infrastructure.

### `obra/superpowers`

Reviewed [`obra/superpowers`](https://github.com/obra/superpowers), especially its planning, worktree, execution, review, and branch-finishing guidance.

Adopted:

- checkable task outcomes;
- isolated mutable work when concurrency actually requires it;
- review between bounded changes;
- cleanup of temporary worktrees after integration;
- frequent durable commits.

Not adopted as defaults:

- a complete methodology that owns every project phase;
- automatic worktree creation for read-only work;
- fixed test-first mechanics regardless of repository or requirement;
- plan archives and runtime/plugin machinery.

### GitHub Spec Kit

Reviewed [`github/spec-kit`](https://github.com/github/spec-kit) for its spec-first workflow and multi-agent portability.

Adopted:

- implementation begins from a reviewed written requirement;
- templates make scope and acceptance criteria visible;
- agent-specific mechanics should sit behind a common product contract.

Not adopted:

- CLI, generators, presets, extensions, or per-agent generated command trees.

The Workbench stays tool-agnostic and dependency-free.

## Source doctrine retained

- The repository owner's current instruction is highest authority.
- Provider boundaries use official SDKs and provider-owned truth.
- Owned behavior uses the minimum direct logic required now.
- One DevOps/Integration Parent maintains repository truth and the known-good head.
- One Feature Parent owns each bounded capability.
- Executors receive narrow assignments and stop on decisions outside scope.
- Independent capabilities may run in parallel; shared mutable boundaries serialize.
- One verified capability equals one atomic commit.
- Regressions start with the newest change after the last known-good head.
- Worktrees are disposable execution environments; Git commits are durable history.
- PRDs use a fixed implementation matrix and close with provider, minimal-build, and product checks.

### Current skill survey

| Source authority | Portable treatment |
| --- | --- |
| Controlled execution | Retained as `workbench-controlled-work`. |
| Repository operations | Retained as `workbench-devops`, the standing integration owner and progress reporter. |
| Integration Parent | Retained as release decomposition and commit acceptance authority. |
| Feature Parent | Retained as one bounded capability owner. |
| Executor | Retained as one narrow task role with evidence and stop conditions. |
| Minimal build | Retained without project-specific names or state. |
| Provider boundary | Retained as `workbench-provider-boundary`; official provider capability and provider-owned truth remain mandatory. |
| Design and copy authority | Project-specific references are excluded. The repository doctrine preserves owner-approved product, design, and copy decisions. |

## Resulting design

The smallest useful public package is static Markdown. It creates no privileged service and introduces no transitive dependencies. Users can inspect every instruction before applying it, keep the parts that fit their environment, and preserve their own repository as the source of truth.
