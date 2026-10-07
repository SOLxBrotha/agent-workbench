# Investigate one regression

Stop new feature work in the affected mutable scope.

Record:

LAST KNOWN-GOOD HEAD:
FIRST FAILING HEAD:
NEWEST CAPABILITY COMMIT:
EXACT CUSTOMER SYMPTOM:
SMALLEST REPRODUCTION:
PROTECTED SURFACES:

Reproduce the reported symptom against the exact failing candidate. Compare the newest capability commit with the immediately preceding known-good head. Change one variable at a time until evidence identifies or clears that commit.

If the newest capability caused the regression, fix or revert only that capability and rerun its outcome check plus affected existing gates. Do not modify previously working systems to accommodate it. Do not launch a broad audit or reopen unrelated subsystems.

Return the responsible commit or `NOT ESTABLISHED`, evidence, the smallest safe response, verification, and exactly one next action.
