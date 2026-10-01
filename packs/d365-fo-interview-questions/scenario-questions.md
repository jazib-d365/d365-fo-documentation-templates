# 15 scenario interview questions
Use these as practice prompts, not a claim about any employer's interview process. Answer with a real, anonymized experience when you have one; distinguish experience from hypothetical reasoning.

## 1. A user requests a customization immediately. What do you do?
**Strong answer direction:** Clarify the outcome and acceptance criteria; assess standard process/configuration first; document gap, options, cost, impact, and ownership before design.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 2. A PO is received but cannot be invoiced. Where do you start?
**Strong answer direction:** Trace order and receipt quantities, invoice inputs, matching policy, holds, and exact error. Separate data issues from configuration; involve finance for posting decisions.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 3. How would you validate a partial delivery?
**Strong answer direction:** Use ordered, shipped/received, invoiced, cancelled, and remaining quantities. Retain references and reconcile stock/financial effects under project policy.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 4. No warehouse picking work is created. What evidence do you collect?
**Strong answer direction:** Order, shipment/load, release log, wave status, applicable work template and location directives, eligible stock, dimensions, and the first relevant error.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 5. Why can on-hand stock still be unavailable to an order?
**Strong answer direction:** Investigate reservations, dimensions, inventory status, location, tracking constraints, and open work. Confirm eligible quantity rather than relying on one aggregated total.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 6. How do you distinguish a transfer order from a transfer journal?
**Strong answer direction:** Explain the dispatch/receipt and operational tracking requirement, then assess the configured process. Avoid selecting by transaction name alone.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 7. How do you plan a DMF migration?
**Strong answer direction:** Define source scope, actual entity keys/fields, mappings, dependency sequence, mock loads, error handling, reconciliation, business smoke tests, and sign-off.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 8. The import job succeeded. Is migration finished?
**Strong answer direction:** No. Demonstrate target key completeness, field/reference correctness, quantity/value reconciliation where relevant, and business owner acceptance.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 9. What distinguishes SIT from UAT?
**Strong answer direction:** SIT checks interactions across components against interface/process contracts. UAT demonstrates that business users can satisfy approved requirements and acceptance criteria.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 10. How do you make UAT cases useful?
**Strong answer direction:** Include role, prerequisites, data, steps, expected result per step, evidence, defect linkage, and measurable pass criteria; cover exceptions and permissions.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 11. When would you use RSAT?
**Strong answer direction:** Assess repeatable supported business tasks after stabilizing test design/data. Explain recordings, parameterization, maintenance, and limitations for the specific process.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 12. An integration creates duplicate orders. What do you investigate?
**Strong answer direction:** Correlation IDs, external references, retries, acknowledgements, timeouts, deduplication design, and target transaction history; test replay and a genuinely new event.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 13. How do you handle a production incident?
**Strong answer direction:** Assess impact, preserve evidence, find the failing stage, coordinate ownership, reproduce safely, validate the approved fix and regression scope, and confirm recovery.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 14. What does a good functional requirement contain?
**Strong answer direction:** Business problem, scope, actors, prerequisites, rules, data, exceptions, proposed solution, security/integration impact, acceptance criteria, and approval.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## 15. What evidence supports a go-live decision?
**Strong answer direction:** Critical process tests, approved residual risks, reconciled migration, access readiness, rehearsed cutover/recovery, training, support ownership, and authorized decision.

**Follow-up:** What evidence would prove the outcome, and which configuration or business assumption could change your answer?

## Official reading
[SCM documentation](https://learn.microsoft.com/en-us/dynamics365/supply-chain/) · [RSAT](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/perf-test/rsat/rsat-overview) · [Data management](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)
