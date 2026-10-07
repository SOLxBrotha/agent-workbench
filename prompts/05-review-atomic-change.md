# Review one atomic change

Review the exact diff from `<BASE SHA>` to `<COMMIT SHA>` against `<PRD ITEM>`.

Verify:

1. The base and commit resolve and the changed-file list is complete.
2. Every hunk is required by the assigned capability.
3. Allowed paths contain every change and protected paths are unchanged.
4. The implementation follows repository doctrine and applicable skills.
5. Provider behavior uses supported SDK/API contracts and provider-owned truth.
6. Owned logic is the minimum direct implementation required now.
7. No secrets, dependencies, policy changes, generated artifacts, unrelated cleanup, duplicate state, or speculative architecture entered the diff.
8. Existing relevant checks pass.
9. The requested customer outcome was observed on this exact candidate when the environment permits.
10. The commit contains one coherent capability and has a clear revert path.

Return `ACCEPT` or `REJECT`, findings with file/hunk evidence, checks, observed outcome, and exactly one next action. Do not rewrite the Feature Parent's solution during review.
