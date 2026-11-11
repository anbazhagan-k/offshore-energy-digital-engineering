# Task 01 — Exploration Block Register Foundations

**Status:** IN PROGRESS  
**Difficulty:** Beginner  
**Estimated time:** 45–60 minutes  
**Tools:** Excel or Google Sheets

## 1. Your role
You are an EIM Specialist supporting a fictional offshore exploration operator. The licence team has provided a list of exploration blocks. Your job is to understand the information, structure the register and make sure each block can be uniquely identified.

You are not being asked to interpret geology, decide whether a block is commercially attractive or approve a petroleum licence. Those decisions belong to the relevant technical and business authorities.

## 2. What is an Exploration Block Register?
It is a structured list of exploration blocks managed by the operator. It allows users to identify each block and find its basic administrative and area information.

| Field | Meaning | Example |
|---|---|---|
| Block_ID | Stable unique identifier for the block | EXB-001 |
| Block_Name | Readable block name | North Example |
| Basin_Name | Geological / exploration basin name | Example Offshore Basin |
| Geographical_Region | Broader geographical location | Example Offshore Region |
| Jurisdiction | Country or licensing jurisdiction | Example Jurisdiction |
| Licence_Reference | Reference to the relevant licence or contract | LIC-EX-001 |
| Gross_Area | Total stated area of the block | 100000 |
| Area_Unit | Unit used for the area value | acres |
| Licence_Status | Administrative status supplied by the licence owner | Active |
| Data_Source | Source from which the record was obtained | Licence schedule |
| Data_Owner | Team accountable for the source information | Licence Team |
| Last_Verified_Date | Date the record was last checked | 2026-11-01 |

These are proposed learning fields. Actual operator registers may use different names, mandatory fields and controlled vocabularies.

## 3. Starter dataset
The file data/01-block-register-starter.csv contains three fictional block records.

Open it in Excel or Google Sheets. Do not change the source values yet. First, inspect the columns and understand what each value represents.

## 4. Your tasks

### Exercise A — Understand the fields
For each field in the starter dataset, identify whether it describes:
- Identity — which block is this?
- Location — where is it?
- Area — how large is it?
- Licence administration — what is its licence status or reference?
- Governance — who supplied or owns the information, and when was it checked?

You can write your classification in a separate column or in your reply.

### Exercise B — Identify the unique identifier
1. Which field should uniquely identify each block?
2. Why should Block_Name not be the only unique identifier?
3. If a block's readable name changes, should its Block_ID normally change? Explain.

### Exercise C — Understand area and units
1. Which two fields together tell you the block's measured area?
2. Why should the number 100000 not be stored without its unit?
3. Is gross acreage a location, an identifier or a measurement?

### Exercise D — Think like an EIM professional
Review the three records and answer:
1. Which team is shown as the data owner?
2. Which field tells you where the information came from?
3. Which field tells you when the information was last verified?
4. What would you do if two records had the same Block_ID?
5. What would you do if the licence team supplied an area value but no unit?

## 5. Rules for this task
- Do not invent missing information.
- Do not assume that a blank field means zero.
- Do not change a source value without recording the reason and source of the correction.
- Treat Block_ID as the proposed stable key for this learning exercise.
- These records are fictional and are not evidence of real offshore licences.

## 6. What to submit
Reply with your answers to Exercises B, C and D. You do not need to create formulas yet.

After we review your answers, we will move to the next step: turning the starter data into a properly structured Excel table, checking unique IDs and applying basic data validation.

## 7. Completion criteria
- [ ] Understand the purpose of a block register.
- [ ] Classify the register fields.
- [ ] Explain the difference between a block identifier and a block name.
- [ ] Explain why area and unit must be stored together.
- [ ] Identify the source, owner and verification date.
- [ ] Complete the review with the tutor.

Do not mark this task complete until the exercises have been reviewed.