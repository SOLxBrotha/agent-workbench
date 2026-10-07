---
name: workbench-minimal-build
description: Mandatory for software the project owns. Define the exact outcome, reuse authoritative data and existing primitives, add the minimum direct logic, verify the outcome, commit atomically, and stop.
---

# Minimal Build

Prime directive:

```text
CUSTOMER OUTCOME
→ EXISTING PRIMITIVES / AUTHORITATIVE DATA
→ MINIMUM NECESSARY OWNED LOGIC
→ EXISTING CUSTOMER SURFACE
```

Before coding, state the exact behavior, relevant UI/components/data/APIs/provider capabilities, authoritative truth, and smallest implementation. Prefer existing files and direct readable code. Add architecture only for a demonstrated current requirement. Work one capability at a time with the minimum diff; verify the actual outcome; commit atomically; stop.

Without explicit owner authority, add no speculative architecture, future-proofing, premature generalization, single-use wrapper, service/repository/factory layer, shadow state, duplicate truth, cache, queue, worker, state machine, reconciliation system, schema, persistence, scale infrastructure, broad refactor, unrelated cleanup, invented policy, new test framework, or report set.

Any proposed complexity must state:

```text
CURRENT REQUIREMENT:
WHY DIRECT IMPLEMENTATION IS INSUFFICIENT:
MINIMUM ADDITION REQUIRED:
```

If those facts cannot be established, make no architectural addition. At a provider boundary, also apply `workbench-provider-boundary`.
