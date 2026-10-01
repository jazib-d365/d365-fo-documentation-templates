# Purchase order walkthrough
## Business question
Can the buyer order 100 EA, receive 60 EA, and invoice only what was received while retaining the remaining obligation?

## Assumptions
Use a sandbox legal entity, a stocked item, approved vendor, purchase unit EA, and a configured standard purchase process. Finance validates posting profiles and matching policy. Warehouse-managed receiving follows its configured mobile flow rather than assuming desktop receipt is sufficient.

## Trace the transaction
| Stage | Action | Evidence to retain |
|---|---|---|
| Prepare | Verify vendor, released item, unit, site, warehouse, price, and delivery date | Master-data and dimension references |
| Create | Create PO for 100 EA at 10 per EA; submit approval if configured | PO number and approval history |
| Confirm | Confirm the approved order under the project process | Confirmation reference |
| Receive | Receive 60 EA through the agreed warehouse flow; post product receipt | Receipt number and physical inventory transactions |
| Invoice | Enter invoice for 60 EA at the agreed price | Invoice, matching result, voucher |
| Reconcile | Review remaining 40 EA and the received/invoiced quantities | PO line totals and inventory transaction evidence |

The illustrative invoice base amount is 600 before tax, charges, and discounts. Do not assume voucher accounts or receipt accrual behavior without reviewing financial configuration.

## Exception tests
- Supplier delivers 110 EA: verify the agreed overdelivery tolerance.
- Invoice quantity is 70 after receiving 60: capture the matching outcome under the configured policy.
- Invoice unit price differs: verify tolerance and authorized exception handling.
- Remaining 40 is cancelled: demonstrate how the residual commitment is closed under the business process.
- Buyer lacks approval rights: prove the required approval boundary.

## Acceptance
The business owner can trace approved order, receipt, invoice, stock movement, and residual quantity without unexplained differences.

## Official reference
[Microsoft Learn: Supply Chain Management documentation](https://learn.microsoft.com/en-us/dynamics365/supply-chain/)
