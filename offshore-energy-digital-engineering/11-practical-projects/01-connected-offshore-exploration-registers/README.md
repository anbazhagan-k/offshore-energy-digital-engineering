# Project 01 — Connected Offshore Exploration Information Registers

## Project purpose
Build a small, connected information-management model for a fictional offshore exploration operator. This portfolio project demonstrates how an EIM professional structures, registers, validates and relates exploration information.

All names, identifiers, coordinates and values are synthetic and for learning only. They do not represent a real licence, operator, survey or prospect.

## Business scenario
A fictional operator manages three offshore exploration blocks in a region called the Example Offshore Basin. The operator receives seismic survey information, technical reports and prospect evaluations from internal teams and contractors. The EIM team must maintain traceable information across five registers.

## Register architecture
| Register | What it records | Primary identifier | Connects to |
|---|---|---|---|
| Exploration Block Register | Licence/block identity, jurisdiction, area and status | Block_ID | Surveys, documents and prospects |
| Seismic Survey Register | Survey identity, type, contractor, coverage and status | Survey_ID | Block_ID, documents and prospects |
| Exploration Document Register | Controlled reports and deliverables | Document_ID | Block_ID, Survey_ID, Prospect_ID where applicable |
| Prospect Register | Prospect identity and evaluation status | Prospect_ID | Block_ID and supporting Survey_IDs |
| Information Quality Register | Issues, validation findings, owners and resolutions | Issue_ID | Relevant register record ID |

## How we will work
We will build incrementally. Each task introduces a small number of concepts, provides synthetic starter data and asks you to complete an exercise. We will review your answers before moving to the next task.

1. Task 01 — Understand and structure the Exploration Block Register.
2. Task 02 — Build the Seismic Survey Register and connect it to blocks.
3. Task 03 — Build the Exploration Document Register and connect deliverables.
4. Task 04 — Build the Prospect Register and connect supporting information.
5. Task 05 — Build the Information Quality Register.
6. Task 06 — Validate the connected registers and identify broken relationships.
7. Task 07 — Prepare an EIM status and data-quality report.

## Tools
- Excel: initial register creation, data validation, filtering, reconciliation and analysis.
- Document Management System (DMS): controlled documents, revisions, review and approval workflows.
- GIS: spatial boundaries, coordinate systems and spatial relationships.
- Enterprise exploration / subsurface data platforms: authoritative technical datasets and specialist workflows.
- Power BI and SQL: later-stage reporting and structured-data querying.

Excel is a learning and working tool in this project. In a real operator environment, the approved enterprise system and data owner determine the authoritative record.

## Information-management principles
- Use a stable unique identifier for each record.
- Do not use a descriptive name as the only identifier.
- Keep identifiers consistent across connected registers.
- Separate measured values from units.
- Record data ownership and source where relevant.
- Do not silently overwrite controlled information.
- Validate references before accepting a data delivery.
- Distinguish missing information from information that is not applicable.
- Keep synthetic portfolio data separate from employer-confidential or proprietary information.

## Project status
- [ ] Task 01 — Block Register foundations
- [ ] Task 02 — Seismic Survey Register
- [ ] Task 03 — Exploration Document Register
- [ ] Task 04 — Prospect Register
- [ ] Task 05 — Information Quality Register
- [ ] Task 06 — Cross-register validation
- [ ] Task 07 — EIM reporting

## Completion standard
The project is complete when all five registers have documented fields, unique identifiers, valid relationships, sample records, quality checks and a concise explanation of how an EIM professional would operate the process.

## Disclaimer
This is an independent learning project using fictional data. It is not an operational register, licence record, technical authority deliverable or substitute for an operator's approved procedures and systems.