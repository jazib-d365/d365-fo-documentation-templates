# Warehouse configuration baseline
Use this checklist before diagnosing work. Record the application version and enabled features; do not change a live configuration as a diagnostic shortcut.

| Layer | Questions | Evidence |
|---|---|---|
| Product and dimensions | Is the item configured for the intended warehouse process? Are units and tracking/reservation settings suitable? | Item and dimension setup |
| Warehouse | Is the warehouse using the required process? Are locations and location profiles configured? | Warehouse and location references |
| Receiving | Which mobile menu item and receipt process apply? Is a work policy intentionally suppressing work? | Menu-item and policy details |
| Outbound release | Did the document create the expected shipment/load? | Release logs and document IDs |
| Wave | Did the applicable wave template and processing steps run? | Wave status and error log |
| Work | Does the correct work template match this work-order type and query? | Template, sequence, and generated work |
| Locations | Can location directives find valid pick/put locations? | Directive queries, actions, dimensions, available quantity |
| Execution | Can the worker use the relevant mobile menu and work class? | User, menu, work class, work status |

## Minimal diagnostic dataset
One known item, one unit, one warehouse, one inbound order, one outbound order, and known on-hand quantities. Add batch, serial, replenishment, or mixed units only after the baseline works.

## Official references
- [Work templates and location directives](https://learn.microsoft.com/en-us/dynamics365/supply-chain/warehousing/control-warehouse-location-directives)
- [Wave templates](https://learn.microsoft.com/en-us/dynamics365/supply-chain/warehousing/wave-templates)
- [Work policies](https://learn.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-work-policies)
