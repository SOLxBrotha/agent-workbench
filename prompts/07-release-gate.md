# Verify and release one candidate

Use the current PRD's fixed implementation matrix. Do not add release criteria after work begins unless a newly discovered current requirement demands it and the product owner approves the matrix change.

Pin:

CANDIDATE SHA:
LAST KNOWN-GOOD SHA:
TARGET ENVIRONMENT:
RELEASE AUTHORITY:

Require:

- all capability commits accepted and integrated in dependency order;
- clean integration working tree;
- exact candidate provenance;
- existing cross-capability checks passing;
- observed product/process outcomes on the candidate where executable;
- provider-boundary audit passing;
- minimal-build audit passing;
- secret and protected-path checks passing;
- known limitations recorded;
- rollback or revert path identified;
- explicit authority for deployment, publication, production mutation, or other consequential action.

After successful integration, remove completed temporary worktrees and prune stale metadata. Git history is the archive.

Return `READY`, `RELEASED`, or `BLOCKED`; the terminal matrix count; the exact candidate; checks; blocker and workaround; and exactly one next action.
