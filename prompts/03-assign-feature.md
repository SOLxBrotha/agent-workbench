# Assign one Feature Parent

Create one assignment for one bounded PRD capability using `https://github.com/SOLxBrotha/agent-workbench/blob/v1.0.0/templates/ASSIGNMENT.md`.

The assignment must:

- pin the exact integration base SHA;
- name one owning Feature Parent;
- list mutable and protected paths;
- identify dependencies and shared state/provider boundaries;
- name every mandatory skill;
- state the observable customer outcome and acceptance gate;
- forbid scope expansion and unrelated cleanup;
- require one verified atomic commit per capability;
- require return through `https://github.com/SOLxBrotha/agent-workbench/blob/v1.0.0/templates/HANDOFF.md`.

Allow parallel execution only if mutable paths, state boundaries, and provider mutation paths do not overlap. Otherwise serialize the assignments.

Return the completed assignment and stop. Do not implement the feature in this response.
