# Detailed manual test designs
## P2P-02: Receive 60 of 100 EA
**Requirement:** Partial receipts preserve the remaining order obligation.  
**Role:** Authorized buyer/receiving user.  
**Setup:** Sandbox company; approved vendor; stocked product; EA unit; valid warehouse; approved PO 100 EA at 10 each; no previous receipt/invoice. Follow the configured warehouse receiving flow.  
**Status:** Not run.

| Step | Action | Expected result | Capture |
|---|---|---|---|
| 1 | Inspect the PO and receipt history | Ordered 100; received 0 | PO and line references |
| 2 | Execute the configured receiving process for 60 | Only 60 recorded in this receipt flow | Warehouse/work reference if applicable |
| 3 | Post product receipt with a unique reference | Receipt exists for 60 | Receipt ID |
| 4 | Review line quantities and transactions | Received 60; remaining 40 | Quantity and transaction evidence |
| 5 | Review physical stock movement | Receipt-related movement accounts for 60 | Before/after on-hand and transaction dimensions |

**Pass:** All quantities reconcile, traceable receipt exists, and remaining 40 is accounted for.  
**Failure:** Log exact actual result and evidence; do not mark passed solely because no error appeared.  
**Cleanup:** Reverse or close test documents only through approved sandbox procedures.

## INT-01: Duplicate inbound order message
**Requirement:** Repeating one external event must not create an unintended second order.  
**Setup:** Sandbox endpoint; agreed integration contract; valid fictional customer/item; test correlation ID TEST-ORDER-001; no previous processing.  
**Status:** Not run.  
**Important:** Deduplication is an integration design requirement; do not assume every D365 endpoint supplies it automatically.

| Step | Action | Expected result | Capture |
|---|---|---|---|
| 1 | Submit one valid message | One accepted business event | Request ID and acknowledgement |
| 2 | Confirm target transaction | One intended order with correct lines | Target order and line references |
| 3 | Resubmit the identical message/correlation ID | Agreed duplicate-handling response | Both message logs |
| 4 | Count target transactions by external reference | One intended order; no duplicate quantity | Query/report evidence |
| 5 | Repeat with a new ID representing a genuinely new order | New event processed independently | New acknowledgement and order |

**Pass:** Original event is processed once and a distinct event remains processable.  
**Failure:** Record duplicates, missing orders, or ambiguous acknowledgements.  
**Cleanup:** Remove test queues and transactions through agreed sandbox procedures.

## Official references
[RSAT overview](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/perf-test/rsat/rsat-overview) · [RSAT best practices](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/perf-test/rsat/rsat-best-practices)

Manual acceptance design comes before automation. Evaluate the appropriate tool for each process; do not assume a browser recording covers warehouse mobile or external integration behavior.
