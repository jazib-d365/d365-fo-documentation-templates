# 20 UAT scenario starters
These are designs, not execution results. Replace the expected result with the approved business policy, add detailed steps, and assign an owner. All scenarios start as **Not run**.

| ID | Scenario | Prerequisite | Test action | Acceptance focus |
|---|---|---|---|---|
| P2P-01 | Full PO receipt and invoice | Approved PO and available vendor/item | Order 10; receive 10; invoice 10 | Quantities and references reconcile |
| P2P-02 | Partial receipt | PO for 100 EA | Receive 60 EA | Remaining 40 is visible |
| P2P-03 | Invoice quantity mismatch | Received 60; matching configured | Submit invoice for 70 | Configured matching outcome recorded |
| P2P-04 | Invoice price variance | Approved price and tolerance | Enter price above tolerance | Configured exception control enforced |
| P2P-05 | Overdelivery | Known tolerance | Receive above ordered quantity | Tolerance policy applied |
| SO-01 | Full sales shipment | Stock and valid customer | Order; pick; ship; invoice 10 | Commercial and stock quantities reconcile |
| SO-02 | Partial shipment | SO for 10 EA | Ship 6 | Remaining 4 is accounted for |
| SO-03 | Customer credit hold | Configured hold | Attempt order processing | Configured hold blocks intended step |
| SO-04 | Unavailable stock | Insufficient eligible stock | Reserve/release requested quantity | Shortage handled under agreed policy |
| SO-05 | Return | Original invoice and return policy | Process approved return | Receipt/credit linked and reconciled |
| INV-01 | Warehouse transfer | 20 EA at A | Transfer 5 to B | Final 15 at A; 5 at B |
| INV-02 | Partial transfer receipt | Shipped 5 | Receive 3 | Remaining 2 accounted for |
| INV-03 | Counting difference | Known book quantity 10 | Record actual quantity 8 | Approved variance -2 posted |
| WMS-01 | Inbound put-away | Valid receiving setup | Receive and execute work | Stock placed at eligible location |
| WMS-02 | Outbound picking | Released order with eligible stock | Process wave and work | Intended pick/put work completed |
| WMS-03 | Missing put location | Controlled invalid location setup | Attempt work creation | Error diagnosable; no silent stock loss |
| SEC-01 | Unauthorized approval | Role without approval rights | Attempt approval | Required access boundary enforced |
| DMF-01 | Missing reference | Mapping with invalid reference | Import one invalid row | Error retained and row not silently accepted |
| INT-01 | Duplicate inbound message | Defined deduplication requirement | Send same correlation ID twice | One intended business transaction |
| INT-02 | Interface recovery | Retry policy and failed message | Correct cause and retry | No lost or duplicated business event |

## Required execution fields
Requirement ID, scenario ID, business owner, tester role, environment/build, test data, steps, expected result per step, actual result, evidence, status, defect ID, retest result, and sign-off date.

## Coverage review
Include standard flow, partial quantity, invalid data, permission boundary, reversal/recovery, integration failure, and reconciliation for each critical business process. A scenario title alone is not sufficient for execution.
