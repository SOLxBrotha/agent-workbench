# Repository doctrine

Replace bracketed values before use.

## Authority

1. Product owner's current explicit instruction.
2. Approved product and design references.
3. Applicable mandatory skills.
4. This repository doctrine.
5. Current product and provider contracts.
6. Current implementation documentation.
7. Git history, which is evidence rather than current authority.

Uncertainty requires verification or a decision from the owner. An agent may not invent product, commercial, security, legal, or design policy.

## Implementation

- Customer outcome → existing primitives and authoritative data → minimum necessary owned logic → existing customer surface.
- Provider capability → official provider SDK/API → provider-owned state.
- Customer-facing presentation follows the owner's approved design reference and existing primitives. Feature approval does not authorize redesign.
- Customer-facing wording follows the owner's approved product language. Agents do not invent policy or product claims.
- Preserve one authoritative source of truth.
- Add architecture only for a demonstrated current requirement.
- Working code is not an invitation to refactor.
- One capability → minimum diff → observed outcome → atomic commit → stop.

## Execution

- Designated DevOps/Integration Parent: `[THREAD OR OWNER]`.
- Canonical integration branch: `[BRANCH]`.
- Every capability records its base SHA, owner, mutable paths, protected paths, dependencies, outcome, and acceptance gate.
- One Feature Parent owns each capability. Executors receive narrower tasks.
- Parallelize only independent mutable scopes. Serialize shared boundaries.
- Integrate verified commits and evidence, never uncontrolled working trees.
- Compare a regression first with the newest atomic change after the last known-good SHA.
- Remove temporary worktrees after verified integration.

## Consequential actions

Explicit owner authority is required for merge, deployment, publication, production mutation, credentials, payments, signing, destructive deletion, and changes to product, security, commercial, legal, or design policy.

## Documentation

Maintain one current PRD per product or process. Its fixed implementation matrix uses `✅ PASS` only for observed completion. End it with provider-boundary audit, minimal-build audit, and successful product/process acceptance checks.
