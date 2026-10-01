# SIT integration test
- Test ID / requirement / interface:
- Source / middleware / target:
- Payload schema/version:
- Authentication and test role:
- Correlation ID / external business key:
- Data prerequisites:
- Expected acknowledgement and timeout:
- Retry and duplicate-handling contract:

| Step | Action | Expected source/middleware/target state | Evidence |
|---|---|---|---|
| 1 | Submit valid message | Contract-compliant acknowledgement and target state | |
| 2 | Submit invalid reference | Contract-compliant rejection; no unintended target record | |
| 3 | Simulate retry | Agreed recovery with no lost or duplicated event | |
| 4 | Reconcile source and target | Quantities/amounts match agreed scope | |

- Actual result / status:
- Defect IDs:
- Retest evidence:
- Owner approval:
