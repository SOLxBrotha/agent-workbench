---
name: workbench-provider-boundary
description: Mandatory when a capability is supplied by an external provider. Use the provider's supported SDK or documented API, preserve provider-owned truth, and add only the minimum owned product behavior around it.
---

# Provider Boundary

Identify the provider capability, current official SDK/API, authoritative documentation, provider-owned state, credentials, callbacks, and documented idempotency requirements before implementation.

Use supported provider primitives for transport, lifecycle, retries, state transitions, and provider-native truth wherever supplied. Do not reimplement or shadow them. A missing SDK capability requires evidence, a documented provider path, and an explicit decision before custom boundary code.

Keep credentials server-side and least-privileged. Preserve required signature verification, raw request handling, idempotency, ownership checks, and secret redaction. Add only the project-owned behavior needed to expose the current customer outcome.

Verify the exact provider-backed outcome in the appropriate sandbox or environment. Record SDK/API version, evidence, limitations, and the smallest rollback path.
