# Mapping and dependency plan
## Begin with an export
Select the intended data entity in your environment and export a small valid sample. Use its actual field names and keys. This document is a design worksheet, not an import-ready file.

## Illustrative mapping
| Business field | Source example | Transformation | Target field from actual entity export | Validation |
|---|---|---|---|---|
| Product identifier | PROD-001 | Trim surrounding spaces; preserve meaningful leading zeros | Fill from export | Unique under entity key |
| Product name | Demo item | Apply approved length rules | Fill from export | Required/nonblank |
| Purchase unit | Each | Map approved source code to EA | Fill from export | Referenced unit exists |
| Warehouse | Main | Map to WH01 | Fill from export | Valid in intended company/site |
| Company | LegacyCo | Map to DEMO | Fill from export | Correct legal-entity context |

Do not invent universal entity field names. Document field defaults and rejected values explicitly.

## Suggested dependency groups
1. Target configuration: legal entities, currencies, units, dimensions, groups, sites/warehouses, and posting setup as required.
2. Master records: relevant parties/accounts/products and company-specific records.
3. Relationships and extensions: addresses, dimensions, trade data, and other entity-dependent records.
4. Approved opening positions and open transactions.
5. Reconciliation and business process smoke tests.

The exact sequence depends on entity relationships and project scope. Record a dependency graph based on actual keys and references.

## Load register
| Load ID | Entity and version | Company | Dependencies | Source owner | Expected rows | Reconciliation owner |
|---|---|---|---|---|---|---|
| MOCK-01 | Fill from environment | DEMO | Units and reference setup | Data owner | 100 | Business owner |

## Official references
[Data management overview](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages) · [Import/export jobs](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job)
