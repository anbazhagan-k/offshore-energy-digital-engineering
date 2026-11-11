# Lesson 02 — Information Management During Early Offshore Exploration

**Module:** 01 — Offshore Energy Fundamentals  
**Study date:** 2026-11-11  
**Status:** STUDY MATERIAL CREATED — LEARNER STUDY AND ASSESSMENT PENDING  
**Audience:** Aspiring Digital Engineering / Engineering Information Management (EIM) / Asset Information Management (AIM) professionals

## 1. Purpose

This lesson explains what information is created during the early stages of an offshore oil and gas opportunity and what an EIM or Digital Engineering professional may do to manage it.

The focus is on three early exploration stages:

1. Acreage and licence / block definition
2. Seismic surveys, processing and interpretation
3. Prospect identification and evaluation

The objective is not to train the learner to perform geophysical interpretation, geological modelling or exploration decisions. The objective is to understand the information, the people who create it, the relationships between information objects, and the controls that help keep information trusted and usable.

## 2. Learning outcomes

After studying this lesson, you should be able to:

- Explain what information is associated with an offshore acreage block.
- Identify typical information generated during seismic acquisition, processing and interpretation.
- Explain what a prospect is and what information supports its evaluation.
- Describe the EIM contribution at each stage.
- Distinguish technical discipline responsibilities from information-management responsibilities.
- Build simple block, seismic survey and prospect registers.
- Explain information traceability from acreage to prospect.
- Describe typical daily activities for an EIM professional supporting an exploration team.

## 3. The early exploration information chain

An operator may hold rights over an offshore block before it knows whether commercially recoverable hydrocarbons are present. It gathers and evaluates information to decide where further exploration may be justified.

A simplified information chain is:

```text
Acreage / Licence Block
        |
        v
Seismic Survey and Acquisition Data
        |
        v
Processed Seismic Dataset
        |
        v
Geological / Geophysical Interpretation
        |
        v
Prospect Identification and Evaluation
        |
        v
Exploration Decision / Possible Well Proposal
```

This is a simplified sequence. In real projects, teams may use existing well data, regional studies, multiple surveys and iterative interpretations. New information can cause earlier interpretations to be revised.

## 4. Stage 1 — Acreage and block information

### 4.1 What is being managed?

Acreage is a defined geographical area over which a company or licence holder has rights to explore for or develop oil and gas, subject to the applicable licence or contract.

The block is a spatial area. Its identity and boundaries need to be clear so that teams know which area the licence, surveys, reports and exploration decisions relate to.

### 4.2 Typical information objects

| Information category | Example fields or records |
|---|---|
| Block identity | Block ID, block name, basin, country / jurisdiction |
| Spatial definition | Boundary polygon, coordinate list, latitude / longitude |
| Coordinate reference | Coordinate reference system (CRS), datum, projection, units |
| Area | Licensed area, area unit, calculation basis |
| Licence / contract | Licence number, licence type, effective date, expiry date |
| Participants | Operator, partners, working interest, participating companies |
| Legal records | Licence, concession agreement, amendments, obligations |
| Environmental / access constraints | Protected areas, exclusion zones, environmental restrictions |
| Supporting studies | Regional geology, bathymetry, existing survey references |

A block map and a coordinate list should be traceable to the same block and should use clearly stated spatial reference information. A map image alone may not be sufficient for precise spatial work.

### 4.3 Example block register

The following is synthetic training data, not a real licence record.

| Block ID | Block name | Area (km²) | Boundary map | Coordinate list | Licence record |
|---|---|---:|---|---|---|
| BLK-001 | Bay Block Alpha | 3,000 | BLK-001-MAP-001 | BLK-001-COORD-001 | LIC-001 |
| BLK-002 | Bay Block Beta | 2,450 | BLK-002-MAP-001 | BLK-002-COORD-001 | LIC-002 |

### 4.4 Typical EIM activities

An EIM professional may:

- Register block maps, coordinate files, licence documents and supporting studies.
- Check that each record has a unique identifier, title, owner, date and status.
- Confirm that block IDs are used consistently across registers and document metadata.
- Check that coordinate reference information is stated and that spatial files are associated with the correct block.
- Track revisions to boundary maps and coordinate files.
- Record access restrictions and document confidentiality classifications.
- Coordinate with GIS / survey, licensing, legal and exploration teams to resolve missing or inconsistent information.
- Report missing or overdue information.

The EIM professional does not independently define legal licence boundaries, certify survey coordinates or interpret legal rights. Those decisions belong to the authorised licensing, legal, survey or geospatial specialists.

## 5. Stage 2 — Seismic studies and information

### 5.1 What is a seismic survey?

A seismic survey is a geophysical investigation that records reflected sound energy to help geoscientists understand underground rock layers and geological structures.

In a marine survey, a specialised vessel may tow sound sources and receiver streamers, or use ocean-bottom sensors. The collected measurements are processed and interpreted by specialist teams.

Seismic data can help identify geological structures that may form hydrocarbon traps. Seismic evidence does not by itself prove that oil or gas is present.

### 5.2 Seismic information lifecycle

| Stage | Typical information |
|---|---|
| Survey planning | Survey area, objectives, planned acquisition parameters, permits |
| Acquisition | Navigation, source and receiver information, field records, raw seismic data |
| Processing | Processing project files, parameters, reports, processed datasets |
| Interpretation | Horizons, faults, structures, maps, interpretation project files |
| Technical review | QC reports, interpretation review comments, approved deliverables |
| Data delivery / archive | Dataset inventory, formats, metadata, storage location, transfer record |

Some seismic datasets are very large and are managed in specialist geoscience data platforms and storage environments. A simple document register is not a replacement for a seismic data management platform.

### 5.3 Example seismic survey register

Synthetic training data:

| Survey ID | Survey name | Year | Data stage | Related block | Status |
|---|---|---:|---|---|---|
| SEIS-001 | Bay 3D Survey | 2024 | Raw acquisition | BLK-001 | Received |
| SEIS-001-PROC | Bay 3D Survey | 2024 | Processed | BLK-001 | Available |
| SEIS-001-INT | Bay 3D Survey | 2024 | Interpretation | BLK-001 | Under review |

A real data model may distinguish the survey, acquisition campaign, dataset, processing version and interpretation project as separate records. Avoid treating all of these as one file or one document.

### 5.4 Typical EIM activities

An EIM professional may:

- Maintain an inventory of expected and received seismic deliverables.
- Check survey identifiers, dataset names, version information and associated block references.
- Confirm that data format, coordinate reference system, units and coverage information are documented where required.
- Track data transfer, receipt, storage location and responsible custodian.
- Check whether processing reports and quality-control records are present.
- Link interpretation reports and maps to the datasets and survey from which they were produced.
- Track technical review comments and approval status.
- Coordinate with geophysicists, data managers, GIS specialists and IT / storage teams.
- Report missing datasets, incomplete metadata, duplicate records or unresolved data-quality issues.

The EIM professional does not process seismic traces, select processing parameters or interpret geological horizons unless separately qualified and assigned to that technical role.

## 6. Stage 3 — Prospect identification and evaluation

### 6.1 What is a prospect?

A prospect is a geological feature or potential drilling target that has been identified and evaluated as having a reasonable possibility of containing hydrocarbons, based on available geological and geophysical evidence.

A prospect is not a discovery. Drilling is needed to test whether hydrocarbons are present.

Geoscientists may use seismic interpretation, regional geology, well information and other evidence to identify and evaluate prospects.

### 6.2 Typical prospect information

| Information category | Example |
|---|---|
| Identity | Prospect ID, prospect name, basin, block |
| Location | Coordinates, map reference, spatial outline |
| Geological interpretation | Structure, interpreted horizons, faults, trap concept |
| Seismic references | Survey ID, dataset version, interpretation project |
| Well references | Nearby wells, well results, offset well information |
| Evaluation | Geological chance factors, uncertainty and risk documentation |
| Resource assessment | Volumetric estimates and assumptions, where available |
| Commercial screening | Economic assumptions and screening outputs, where available |
| Decision records | Technical review, recommendation, decision date, action |
| Deliverables | Prospect evaluation report, maps, supporting datasets |

Resource estimates and geological chance assessments are specialist technical outputs. Their methods, assumptions and classifications must be understood in context and should not be invented or independently validated by an EIM coordinator.

### 6.3 Example prospect register

Synthetic training data:

| Prospect ID | Prospect name | Block ID | Supporting interpretation | Evaluation status |
|---|---|---|---|---|
| PR-001 | Alpha | BLK-001 | SEIS-001-INT | Under evaluation |
| PR-002 | Beta | BLK-001 | SEIS-001-INT | Preliminary |
| PR-003 | Gamma | BLK-002 | SEIS-002-INT | Under evaluation |

### 6.4 Typical EIM activities

An EIM professional may:

- Maintain the prospect register and unique prospect identifiers.
- Check that each prospect is associated with the correct block and supporting interpretation.
- Ensure evaluation reports, maps and decision records are registered and discoverable.
- Track document and dataset versions used in an evaluation.
- Record information owners, review status, approval status and dates.
- Identify missing supporting information and coordinate follow-up with the responsible discipline.
- Maintain traceability between source data, interpretation deliverables and prospect records.
- Prepare information readiness reports for exploration management.

The EIM professional does not decide whether a prospect contains hydrocarbons, calculate reserves independently or approve a drilling recommendation.

## 7. Information traceability — connecting the stages

A central EIM responsibility is helping users trace information from its origin to the technical output or decision it supports.

Example relationship:

```text
BLK-001 — Acreage Block
   |
   +--> SEIS-001 — Seismic Survey
           |
           +--> DATA-001 — Processed Dataset
                   |
                   +--> INT-001 — Interpretation
                           |
                           +--> PR-001 — Prospect Alpha
                                   |
                                   +--> EVAL-001 — Evaluation Report
```

The identifiers above are illustrative. Actual operators may use different data models and naming conventions.

### Why traceability matters

If an exploration manager asks, "Which seismic interpretation supports Prospect Alpha?", the team should be able to identify the relevant interpretation, dataset version and survey.

If a dataset is superseded, the team should be able to determine which prospect evaluations may have relied on the earlier version and whether technical review is required.

Traceability supports:

- Provenance — where information originated.
- Version awareness — which version was used.
- Context — which block, survey or prospect the information concerns.
- Accountability — who created, reviewed or approved a deliverable.
- Reuse — whether information can be found and reused appropriately.
- Decision support — what evidence supports a technical recommendation.

## 8. What an EIM professional's day may look like

The schedule below is illustrative. Real duties vary by operator, contractor, project stage and role seniority.

| Time | Example activity |
|---|---|
| 09:00 | Attend exploration information coordination meeting; review new deliverables and outstanding actions. |
| 10:00 | Register block maps, survey reports, datasets and prospect evaluation documents. |
| 11:30 | Check identifiers, metadata, revisions, spatial references and required supporting records. |
| 13:00 | Coordinate information relationships between block, survey, dataset, interpretation and prospect records. |
| 14:30 | Prepare completeness and information-readiness reports or dashboards. |
| 16:00 | Follow up with discipline owners on missing, rejected or overdue deliverables. |
| 17:00 | Update registers, action logs and status reports for the next coordination cycle. |

Common outputs may include:

- Block and licence information register
- Seismic survey and dataset inventory
- Document and deliverable register
- Prospect register
- Metadata completeness report
- Information-gap / action log
- Revision and approval status report
- Information traceability matrix
- Data handover or archive inventory

## 9. Typical systems and tools

| Tool / system type | Possible use | EIM role |
|---|---|---|
| Excel | Registers, checks, action tracking | Build and maintain controlled working registers where appropriate |
| Document management system | Controlled documents and revisions | Register, classify, route and retrieve documents |
| SharePoint / collaboration platform | Team collaboration and working files | Organise information and access according to governance |
| GIS platform, e.g. ArcGIS | Spatial block and survey information | Manage references, metadata and coordination with GIS specialists |
| Geoscience platform, e.g. Petrel | Seismic interpretation and subsurface workflows | Understand dataset references and coordinate information handoffs; not necessarily operate the specialist interpretation tools |
| Power BI | Reporting and dashboards | Present completeness, status and information-quality measures |
| SQL / data platform | Structured data queries and integration | Support data validation and reporting as the role requires |

Not every organisation uses all these systems. A document management system, a geospatial system and a specialist seismic data platform serve different purposes; one should not be assumed to replace the others.

## 10. Roles and responsibility boundaries

| Activity | Primary technical / business owner | EIM contribution |
|---|---|---|
| Define or amend licence boundaries | Licensing, legal, survey / GIS specialists | Manage controlled records and references |
| Acquire seismic data | Geophysics / survey contractor | Track deliverables, metadata and receipt |
| Process seismic data | Geophysics / processing specialists | Track datasets, versions and reports |
| Interpret seismic data | Geophysicists | Manage traceability and interpretation deliverables |
| Identify and evaluate prospects | Geology / geophysics / exploration specialists | Maintain prospect information and supporting references |
| Assess commercial potential | Commercial / subsurface / economics specialists | Track controlled supporting information |
| Approve exploration decisions | Authorised exploration management / governance | Ensure decision records and evidence are accessible |

**Key distinction:** Technical disciplines create and approve specialist technical content. EIM helps ensure that the information is controlled, connected, complete, traceable and usable.

## 11. Information quality checks

For each information object, consider whether it has:

- A unique and stable identifier.
- A clear title and description.
- An owner or responsible discipline.
- A date and revision / version where applicable.
- A defined status (for example, draft, under review, approved, superseded).
- A relationship to the relevant block, survey, dataset or prospect.
- A known storage location and access classification.
- Required metadata and supporting records.
- A clear source and provenance.

Do not assume every field applies to every information object. The project's information requirements and data standards determine the mandatory metadata.

## 12. Practical exercises

Use the synthetic scenario below. Do not use employer-confidential information.

### Exercise A — Build a block register

A company holds two offshore blocks:

| Block ID | Area | Boundary map | Licence |
|---|---:|---|---|
| BLK-001 | 3,000 km² | Received | Received |
| BLK-002 | 2,450 km² | Received | Pending |

Tasks:
1. Identify the information objects that should be registered.
2. Identify which record is missing or pending.
3. List three metadata fields you would check before accepting a boundary map.
4. Explain why the coordinate reference system matters.

### Exercise B — Build a seismic inventory

The exploration team expects raw acquisition data, processed data, a processing report and an interpretation report for Survey SEIS-001. Only the raw data and processed data have been received.

Tasks:
1. Create a simple deliverable register with expected item, received status and action owner.
2. Identify the outstanding deliverables.
3. Explain why the processed dataset should be linked to its source survey.
4. Explain why a dataset version should be recorded.

### Exercise C — Build a prospect register

The geoscience team has identified Prospect Alpha and Prospect Beta in BLK-001. Alpha has an evaluation report; Beta's report is pending.

Tasks:
1. Create a prospect register with prospect ID, name, block, supporting interpretation and status.
2. Identify the missing information for Beta.
3. Explain how you would trace Alpha back to the seismic interpretation.
4. State which team should approve the geological evaluation.

### Exercise D — Information readiness report

Using the information from Exercises A–C:
1. Summarise received, pending and under-review items.
2. Identify the three most important information gaps.
3. Assign a responsible discipline for each follow-up.
4. Draft a short status update for the exploration manager.

## 13. Knowledge assessment

Answer in your own words.

1. What is the difference between acreage and a prospect?
2. What does a marine seismic survey attempt to measure or reveal?
3. Does seismic interpretation prove that hydrocarbons are present? Explain.
4. What is the difference between a seismic survey, a processed dataset and an interpretation?
5. Name five types of information that may be included in a prospect evaluation.
6. What is information traceability?
7. If a prospect evaluation report is missing, what should an EIM specialist do?
8. Who is responsible for interpreting seismic data?
9. Why should the coordinate reference system be recorded for spatial information?
10. Give three examples of daily EIM activities during early exploration.

## 14. Completion checklist

- [ ] Explain the information associated with an acreage block.
- [ ] Describe the seismic information lifecycle.
- [ ] Distinguish raw, processed and interpreted seismic information.
- [ ] Explain what a prospect is and what information supports its evaluation.
- [ ] Build the three example registers.
- [ ] Explain traceability from block to prospect.
- [ ] Distinguish EIM responsibilities from specialist technical responsibilities.
- [ ] Complete Exercises A–D.
- [ ] Answer the knowledge assessment.

## 15. Key takeaways

1. Early exploration creates spatial, legal, geophysical, geological, commercial and decision-support information.
2. EIM helps make this information identifiable, controlled, connected, complete and retrievable.
3. The relationship between acreage, seismic surveys, datasets, interpretations and prospects is important for traceability.
4. EIM supports technical teams; it does not replace geoscientists, geophysicists, licensing specialists or exploration decision-makers.
5. The information created during exploration may become important input to later appraisal, development planning and asset lifecycle activities.

## 16. Suggested next lesson

After completing this lesson, continue with exploration wells and appraisal information: well proposals, well identifiers, well programmes, drilling records, well logs, test results and the information used to evaluate a discovery.
