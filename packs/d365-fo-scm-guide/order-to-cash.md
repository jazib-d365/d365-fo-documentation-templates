# Sales order walkthrough
## Example
A customer orders 10 EA of a stocked product. The warehouse ships 6 EA first; 4 EA remain for a later shipment.

## Before testing
Confirm customer credit/hold policy, item availability, dimensions, reservation rules, price, delivery address, warehouse process, tax, and financial posting setup. Record whether advanced Warehouse management is enabled.

## Business trace
1. Create the order for 10 EA and verify the customer, price, delivery dates, and inventory dimensions.
2. Apply the project's reservation and release process.
3. For advanced warehousing, inspect shipment/load, wave processing, and work before executing mobile picking.
4. Complete the configured picking, packing, and shipment steps for 6 EA.
5. Post the packing slip through the agreed process and retain its reference.
6. Invoice the shipped quantity according to the billing policy.
7. Review the remaining 4 EA, invoice quantity, inventory transactions, and customer transaction.

## What to measure
| Control | Expected outcome in this example |
|---|---|
| Shipment quantity | 6 EA for the first shipment |
| Remaining delivery | 4 EA, unless explicitly cancelled |
| Commercial value | Agreed price and adjustments are carried through |
| Inventory | Physical and financial movements are explainable |
| Credit control | Holds are handled under the configured policy |
| Traceability | SO, shipment, packing slip, invoice, and voucher can be related |

## Negative cases
Test an unavailable quantity, a credit-held customer, an invalid delivery address, a substituted batch, and a partial cancellation. Write the policy-specific expectation first.

## Discovery question
Does the business permit partial deliveries and partial invoices? Ask before turning the example into an acceptance test.

## Official reference
[Microsoft Learn: Supply Chain Management documentation](https://learn.microsoft.com/en-us/dynamics365/supply-chain/)
