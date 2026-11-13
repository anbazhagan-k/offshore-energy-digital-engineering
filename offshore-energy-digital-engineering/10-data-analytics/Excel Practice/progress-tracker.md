# Excel Practice — Progress Tracker

**Last updated:** 2026-11-13  
**Learning focus:** Excel foundations for engineering information and asset data management.

## Lesson progress

| No. | Topic | Study status | Practice status / evidence | Assessment |
|---:|---|---|---|---|
| 01 | SUM, AVERAGE and MAX | PRACTISED | Learner reports strong confidence; sample equipment quantities used | Informal confirmation |
| 02 | MIN, COUNT, COUNTA and COUNTBLANK | STUDIED | Example equipment register and expected results reviewed | Independent quiz not recorded |
| 03 | Relative, absolute and mixed references | PRACTISED | Learner completed exercises and reported confidence | Informal confirmation |
| 04 | Copying formulas and Fill Handle | STUDIED / PRACTISED | Formula-fill exercise covered; learner proceeded | Quiz result not recorded |
| 05 | Data types, number formats and dates | STUDIED | Date serial numbers explained; SUM result/date-format issue diagnosed | Concept check discussed |
| 06 | Sorting, filtering and Excel Tables | IN PROGRESS | Screenshot verifies Table1, ascending quantity order and structured-reference SUM | Filtering practice still to verify |
| 07 | IF and Nested IF | PRACTISED — ADDITIONAL EXERCISE PENDING | Multiple independent equipment exercises completed; comparison operators, threshold boundaries, VALUE and Nested IF covered | Nested IF concept check 3/3; pressure classification exercises 10/10 and 9/9 |
| 08 | AND, OR and combining logical functions | PRACTISED — CORE EXERCISES VERIFIED | IF + OR formula and all seven outputs correct; IF + AND logic correctly applied; combined IF + OR + AND exercise 9/9 | Core examples verified; additional revision optional |
| 09 | COUNTIF and COUNTIFS | COUNTIFS PRACTISED — COUNTIF ASSESSMENT PENDING | 6/6 two-condition, 3/3 three-condition and 4/4 date-range exercises correct; date-range + equipment filter also correct | COUNTIFS knowledge check correct (AND logic); independent COUNTIF assessment pending |
| 10 | VLOOKUP fundamentals | DEFERRED | Introduced previously; paused to strengthen foundations | Pending |
| 11 | XLOOKUP fundamentals | COMPLETED — EARLIER SESSION | Completed in an earlier learning session | Completed |
| 12 | Reverse XLOOKUP and advanced lookup topics | NOT STARTED | Pending | Pending |

## 2026-11-10 — Session record

### Training completed / covered

- Reviewed basic formula use and confirmed confidence with SUM, AVERAGE and MAX.
- Studied MIN, COUNT, COUNTA and COUNTBLANK using a synthetic equipment register.
- Practised relative, absolute and mixed cell references.
- Studied copying formulas and using the Fill Handle.
- Covered text, number, percentage and date data types and formatting.
- Learned that Excel stores dates as serial numbers and uses them for date arithmetic.
- Studied sorting, filtering and converting a range into an Excel Table.
- Used a structured reference: `=SUM(Table1[Quantity])`.
- Troubleshot a total of 20 displaying as 19-Jan-1900 because the result cell had a date format. The formula was correct; the cell format needed to be changed to General or Number.

### Evidence and accuracy notes

- Learner explicitly reported confidence with SUM, AVERAGE and MAX.
- Learner reported completing exercises and feeling confident with cell references.
- Shared screenshot showed an Excel Table named Table1, quantities sorted ascending (2, 3, 4, 5, 6), filter dropdowns and the structured-reference SUM formula.
- Filtering by discipline was taught, but completion of the hands-on filter tasks has not yet been confirmed.
- Independent assessment scores for the counting functions have not been recorded. These topics are therefore not marked fully completed.

## 2026-11-11 — IF and Nested IF

### Concepts studied

- IF syntax and the logical test, TRUE result and FALSE result arguments.
- Comparison operators: `=`, `>`, `<`, `>=`, `<=` and `<>`.
- Strict versus inclusive thresholds, including the distinction between `<0` and `<=0`, and between `>5` and `>=5`.
- Relative cell references while copying IF formulas down a column.
- Numeric-looking values stored as text; used `VALUE()` to convert a value before comparison after an IF exercise returned unexpected classifications.
- Nested IF structure, sequential evaluation and matching closing parentheses.
- Boundary-value checks for pressure classifications.

### Practice and evidence

- Inspection status exercise: corrected the zero boundary; negative values were Overdue and zero/positive values Within Schedule.
- Quantity classification exercise: corrected the exact-5 boundary by using `>=5`.
- Maintenance priority exercise: all five results correct using a threshold of more than 180 days.
- Pressure classification exercise: all five results correct using greater than or equal to 20 bar.
- Four-band Nested IF pressure exercise: all ten results correct, including boundary values 15, 25 and 35.
- Five-band Nested IF pressure exercise: all nine results correct, including boundary values 10, 20, 30 and 40.
- Conceptual Nested IF check: 3/3 correct.
- Additional maintenance-risk Nested IF exercise has been assigned but not yet completed.

## 2026-11-12 — AND, OR, COUNTIF and COUNTIFS

### AND, OR and combined logical functions

- Learned that AND returns TRUE only when all conditions are TRUE.
- Learned that OR returns TRUE when at least one condition is TRUE.
- Applied IF + AND to a maintenance-priority scenario; all six predicted outcomes were correct.
- Independently supplied the IF + OR formula `=IF(OR(B2>=365,C2="Critical"),"Yes","No")`; all seven outputs were correct (7/7).
- Built and applied `=IF(OR(B2>=365,AND(B2>=180,C2="Critical")),"Immediate Attention","Normal")`; all nine outputs were correct (9/9).
- Reinforced threshold boundaries: 365 qualifies for `>=365`, 364 does not; 180 qualifies for `>=180`, 179 does not.

### COUNTIF and COUNTIFS

- Studied COUNTIF syntax and counting text criteria such as Pump and Critical.
- Studied numerical criteria and comparison operators: `>`, `<`, `>=`, `<=`, `=` and `<>`.
- Learned that comparison criteria such as `">=180"` must be enclosed in quotation marks.
- Studied COUNTIFS syntax and AND logic between criteria pairs.
- Practised examples combining two text conditions and mixed text/numerical conditions.
- Independent COUNTIF assessment was not submitted in this session.
- COUNTIFS practice questions were introduced, but independent answers have not yet been submitted. Do not mark COUNTIF/COUNTIFS completed.

### Next actions

1. Resume with the COUNTIFS practice questions in [Lesson 09](09-countif-and-countifs.md).
2. Complete an independent COUNTIF/COUNTIFS assessment before progressing.
3. Learn COUNTIFS with three or more conditions and date ranges.
4. Return to the additional maintenance-risk Nested IF exercise.
5. Finish and verify filtering by Discipline; clear the filter to restore all records.
6. Complete a short review of MIN, COUNT, COUNTA and COUNTBLANK.
7. Return to VLOOKUP after the formula foundations are secure.

## Status definitions

- `NOT STARTED` — not yet studied.
- `IN PROGRESS` — currently learning or practical work remains.
- `STUDIED` — concept taught; independent practice or assessment remains.
- `PRACTISED` — exercises attempted; formal assessment may still be pending.
- `COMPLETED` — lesson, independent exercise and assessment completed.
- `DEFERRED` — deliberately postponed until prerequisite learning is stronger.

## Completion rule

Do not mark a lesson COMPLETED until the learner can explain the concept, complete an independent exercise, check the result and answer a short knowledge assessment.


## 2026-11-13 — COUNTIFS multi-condition and date-range practice

### Practice completed and verified

- Completed all six original COUNTIFS exercises independently; all six formulas and counts were correct.
- Completed three additional three-condition exercises: Pump + Critical + days >300 (1), Compressor + High + days >=300 (1), and Valve + High + days <=180 (1). All correct.
- Learned date-range counting by applying lower and upper date criteria to the same date column.
- Independently counted March–April 2026 inspections (4), April–May 2026 inspections (3), and March 2026 inspections (2). All correct.
- Independently combined Equipment = Pump with the March–April date range; result 1 was correct.
- Reviewed `&` concatenation with `DATE()` to construct robust date criteria.
- Correctly answered the knowledge check that COUNTIFS requires all criteria to be satisfied (AND logic).

### Current status and next action

- COUNTIFS multi-condition and date-range practice: verified.
- COUNTIF single-condition independent assessment: still pending. Lesson 09 remains open; do not mark it COMPLETED yet.
- Next: conduct the independent COUNTIF assessment, then update the lesson status based on results.
