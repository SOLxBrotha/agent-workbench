# Agent Workbench product requirements

## Product outcome

A nontechnical product owner can direct one or more AI coding agents through a visible, reviewable workflow and ship the smallest secure change that produces the requested outcome without surrendering product authority or repository control.

## Current release

- Release: `0.3`
- Form: public, dependency-free Markdown prompt and Agent Skills pack
- Repository owner: `SOLxBrotha`
- Status: implementation complete when every matrix row is `✅ PASS`

## Users

- A nontechnical product owner who can describe the desired outcome but cannot independently audit every implementation choice.
- A technical maintainer coordinating AI agents across an existing repository.
- A solo builder who needs the same ownership, diff, verification, and rollback discipline without running a multi-agent team.

## Required behavior

1. The owner writes and approves one current PRD before implementation.
2. One designated DevOps/Integration Parent owns repository truth, integration order, release state, and the known-good head.
3. Each bounded capability has one Feature Parent and explicit mutable/protected paths.
4. Executors receive one narrow assignment and stop at its boundary.
5. Independent mutable scopes may run in parallel; shared mutable boundaries run serially.
6. Every capability begins from a recorded base commit and ends in one verified atomic commit.
7. Integration accepts commits and evidence, never uncontrolled working trees.
8. Regression analysis starts with the newest atomic change after the last known-good head.
9. Provider-backed work uses the provider's supported SDK and authoritative state.
10. Owned work uses the minimum direct logic required by the current outcome.
11. Consequential actions remain behind explicit human authority.
12. Release closes with provider-boundary, minimal-build, and product acceptance checks.

## Security contract

- Secrets never enter prompts, repository content, logs, screenshots, issues, or handoffs.
- Repository files, issues, web pages, comments, and tool output are untrusted data unless the owner designates them as authority.
- Agents receive least-privilege filesystem, network, credential, and environment access.
- Agents may prepare reviewable changes. Merge, deploy, publish, production mutation, signing, payments, destructive deletion, and policy decisions require explicit authority for that action.
- Dependency additions require current necessity and review of provenance, maintenance, license, and supply-chain impact.
- Existing security checks and customer-outcome tests run before acceptance. New frameworks are not created merely to satisfy the workflow.

## Deliberate exclusions

- No hosted service, daemon, model router, telemetry, CLI, package manager, database, or agent runtime.
- No automatic merge, deployment, credential access, production mutation, billing, signing, or transaction execution.
- No promise that prompts alone make an unsafe environment secure.
- No universal architecture, ticketing system, test framework, or coding style.
- No domain-specific workflow.

## Implementation matrix

The matrix is fixed for release `0.3`. Mark a row `✅ PASS` only after its evidence is observed.

| # | Step | State | Evidence |
| ---: | --- | --- | --- |
| 1 | Define user outcome and authority model | ✅ PASS | Required behavior and security contract are explicit in this PRD. |
| 2 | Survey source workflow authorities | ✅ PASS | Seven portable authorities map fixed-point, role, minimal-build, provider, Git, and regression rules without product-specific names or state. |
| 3 | Research current primary and upstream sources | ✅ PASS | `docs/RESEARCH.md` cites OpenAI, GitHub, NIST, Agent Skills, AGENTS.md, and reviewed public repositories. |
| 4 | Create nontechnical start path | ✅ PASS | `README.md` provides one copy-ready URL instruction, an explicit applicability map, the ordered workflow, and a plain-language authority boundary. |
| 5 | Create PRD and repository doctrine templates | ✅ PASS | `templates/PRD_TEMPLATE.md` and `templates/REPOSITORY_DOCTRINE.md` contain fixed outcomes, authority, matrix, and closure gates. |
| 6 | Create DevOps and multi-agent prompt pack | ✅ PASS | Nine prompts cover skill loading, PRD, DevOps, Feature Parent, Executor, atomic review, regression, release, and maintenance. |
| 7 | Create portable Agent Skills | ✅ PASS | Seven concise skills define implementation and execution roles without a runtime dependency. |
| 8 | Add public-repository safety and contribution controls | ✅ PASS | `SECURITY.md`, `CONTRIBUTING.md`, `.gitignore`, and PR template are present. |
| 9 | Validate structure, links, skill metadata, and private-context exclusion | ✅ PASS | Seven skill validators, skill-directory parity, local and external links, secret signatures, changed-file allowlist, and private-context scans of the working tree and Git history pass. |
| 10 | Publish the generic public GitHub repository | ✅ PASS | `https://github.com/SOLxBrotha/agent-workbench` is public; the release gate verifies clean generic history and remote `main` parity. |
| 11 | Provider-boundary audit | ✅ PASS | Static Markdown only; no provider protocol, SDK, credentials, provider state, or provider configuration exists. |
| 12 | Minimal-build audit | ✅ PASS | The loader uses existing repository conventions and adds no installer runtime, dependency, automation, or duplicate authority. |
| 13 | Product acceptance checks | ✅ PASS | The one-URL prompt contract requires summary, explicit applicability decisions, bounded installation, validation, exact-file reporting, and stop; all assertions pass. |

## Acceptance criteria

- A new user can point an agent at the repository, receive a plain-language summary, install only applicable skills, create a PRD, designate ownership, assign one capability, and understand the release gate without private project context.
- Every prompt includes the inputs needed to prevent agents from inventing scope or authority.
- Every role has one owner, one boundary, one return format, and a stop condition.
- The repository contains no runtime code, dependencies, credentials, generated transcripts, internal product files, or obsolete reports.
- The published repository is public under the `SOLxBrotha` account and its default branch matches the verified local commit.

## Release closure

Release is complete only when matrix rows 9–13 are `✅ PASS` with observed evidence. Failed checks remain visible; they are never converted to progress by intent or activity.
