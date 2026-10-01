# Migration reconciliation
A completed import job is evidence of processing, not proof that the business data is correct.

## Worked example
A source extract contains 100 distinct product records. The approved exclusion list contains 5 discontinued records. Expected in-scope population: **95**.

First load: 92 accepted and 3 rejected. Correct the three rejected rows and retry under an agreed key/update strategy. Final target population for the defined scope should be 95 distinct keys, not 98. Check both target state and execution history.

| Control | Expected | Actual | Evidence | Owner |
|---|---|---|---|---|
| Source distinct keys | 100 | | Extract/hash/reference | Source owner |
| Approved exclusions | 5 | | Approved exclusion list | Business owner |
| In-scope distinct keys | 95 | | Filtered source | Migration lead |
| Initial accepted/rejected | 92 / 3 | | Job and row errors | Migration lead |
| Final target distinct keys | 95 | | Scoped target export | Business owner |
| Duplicate keys | 0 | | Duplicate check | Data owner |
| Required fields/references | Valid for all 95 | | Validation report | Data owner |

## More than row counts
- Compare key sets: missing in target and unexpected in target.
- Compare control totals by company, currency, unit, and relevant dimensions.
- For opening stock, reconcile quantity and value under the approved valuation design.
- Sample high-risk and boundary records, not only the first rows.
- Execute relevant business smoke tests on migrated records.
- Record transformations and accepted differences.

## Error handling
Preserve the original error, rejected key, cause, correction, retry job ID, and final evidence. Scope retries to known failures or a demonstrated safe update strategy.

## Completion
Data owner signs off the source scope; business owner signs off target correctness. Keep those decisions separate.
