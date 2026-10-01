# Migration cutover runbook
## Preconditions
Approved scope and mapping, tested dependency order, repeatable mock results, named owners, recovery plan, and business reconciliation criteria.

| Step | Task | Owner | Entry criterion | Completion evidence |
|---|---|---|---|---|
| 1 | Confirm freeze window and transaction boundary | Business lead | Approved cutover schedule | Communication and timestamp |
| 2 | Capture agreed source extracts | Source owner | Boundary reached | Extract reference and counts |
| 3 | Validate scope, keys, required fields, references | Data lead | Extract captured | Validation report |
| 4 | Load in tested dependency order | Migration lead | Prerequisites present | Job IDs and execution logs |
| 5 | Resolve and reconcile rejected rows | Data owner | Errors classified | Correction and retry evidence |
| 6 | Reconcile target keys, quantities, and values | Business/finance owners | Loads completed | Signed reconciliation |
| 7 | Run agreed business smoke tests | Process owners | Reconciliation complete | Test evidence |
| 8 | Make go/no-go decision | Authorized sponsor | Gates reviewed | Recorded decision |
| 9 | Monitor and hand over | Support lead | Go decision | Ownership and monitoring log |

## Stop conditions
Define before cutover: unexplained totals, missing critical references, failed critical smoke tests, or missed recovery deadline. Escalate to the named decision owner.

## Recovery worksheet
- Trigger:
- Latest safe recovery decision time:
- Recovery method validated in rehearsal:
- Owner and approvals:
- Treatment of already posted transactions:
- Verification of restored/recovered state:
- Communication and resumed processing:

A DMF import is not a universal undo mechanism. Use the environment and transaction recovery approach rehearsed by the project team.

## Official reference
[Data management and entity integration](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/data-management-integration-data-entity)
