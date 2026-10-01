# Warehouse troubleshooting matrix
Begin with the failing document and its logs. Change one variable in a sandbox, then compare with a working example.

| Symptom | Investigate first | Controlled test | Evidence of resolution |
|---|---|---|---|
| No outbound work | Release result, wave status, template query, processing errors | Release a known-good small order | Work created for the intended document |
| Pick location not found | Available physical stock, dimensions/status, directive filters and actions | Use known stock in a valid pick location | Intended location selected |
| Put location not found | Directive conditions, location profile, capacity and mixing rules | Receive a small quantity to an eligible location | Valid put instruction |
| Work exists but worker cannot see it | Mobile menu process, work class, user access, work status | Compare with an authorized test worker | Work available to intended role |
| Picking shortfall | Reserved versus available stock, batch/status, prior work | Reconcile stock and reservation for one item | Quantities reconcile before retry |
| Unexpected split | Directive split settings, quantities, location availability | Compare a single-location and multi-location quantity | Split matches the business rule |
| No inbound work after receipt | Receiving process and work policy | Compare the menu item and policy with a working receipt | Work created or intentionally suppressed |
| Duplicate operational attempt | Document state, previous work, interface retries | Trace one external correlation ID through its history | One intended business transaction |

## Investigation sequence
1. Record document, company, warehouse, item, dimensions, quantity, timestamp, and user.
2. Separate release, work creation, and work execution failures.
3. Read the first relevant error, not just a later generic message.
4. Compare configuration and data with one successful transaction.
5. Reproduce the issue with fictional data.
6. Validate the fix, adjacent scenarios, and permissions before approved deployment.

A symptom can have several causes. The matrix is an investigation aid, not a diagnosis.

## Official references
[Location directives](https://learn.microsoft.com/en-us/dynamics365/supply-chain/warehousing/create-location-directive) · [Work control](https://learn.microsoft.com/en-us/dynamics365/supply-chain/warehousing/control-warehouse-location-directives)
