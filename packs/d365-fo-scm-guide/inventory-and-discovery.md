# Inventory movements and process discovery
## Pick the right business process
| Need | Candidate process | Clarify before design |
|---|---|---|
| Ship stock between warehouses with dispatch and receipt evidence | Transfer order | Transit, partial shipment, receiving, and warehouse execution |
| Record an allowed direct movement without a shipping lifecycle | Transfer journal | Approved use, dimensions, and posting controls |
| Correct an approved stock discrepancy | Configured adjustment/counting process | Reason, approval, valuation, and audit trail |
| Determine actual stock at a location | Counting process | Count freeze, recount, tolerance, and adjustment policy |

Validate availability and process suitability in your environment; these are discovery starting points.

## Transfer example
Start with 20 EA at warehouse A and zero at B. Transfer 5 EA using the chosen shipping/receiving process. Capture balances before dispatch, during transit if applicable, and after receipt. Final physical totals should account for all 20 EA, with 15 at A and 5 at B once the transfer is complete and no other transactions occur.

Test partial receipt and a wrong batch/location. Document who resolves each exception and how the remaining quantity is accounted for.

## Discovery checklist
- [ ] Name the trigger, owner, approver, and completion event.
- [ ] Record legal entities, sites, warehouses, units, and tracking dimensions.
- [ ] Identify warehouse-managed versus basic inventory processes.
- [ ] List volume, peaks, partials, reversals, returns, and corrections.
- [ ] Identify interface dependencies and source of truth.
- [ ] Define operational and financial reconciliation.
- [ ] Agree roles, evidence, and measurable acceptance.
- [ ] Classify each gap as process change, configuration, reporting, integration, or customization.

## Output
One process map, requirement list, decision log, and linked test scenarios per process.
