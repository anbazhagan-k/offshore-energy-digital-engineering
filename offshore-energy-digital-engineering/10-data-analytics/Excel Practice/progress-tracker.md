# Excel Practice — Progress Tracker

**Last updated:** 2026-11-19  
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
| 09 | COUNTIF and COUNTIFS | COMPLETED | COUNTIF assessment 5/5; COUNTIFS two-condition 6/6, three-condition 3/3, date-range 4/4; two- and three-condition OR practice; combined assessment 5/5 | Passed combined review and inclusion–exclusion knowledge check on 2026-11-14 |
| 10 | SUMIF and SUMIFS | COMPLETED | Five-question independent assessment passed (5/5) on 2026-11-15 | Passed 5/5 |
| 11 | AVERAGEIF and AVERAGEIFS | COMPLETED | Criteria, wildcards, dynamic references, AND/OR, weighted averages and overlap removal practised; combined-average formula independently constructed | Passed 4/5 fully correct on first attempt; one arithmetic correction reviewed (2026-11-19) |
| 12 | VLOOKUP fundamentals | DEFERRED | Introduced previously; paused to strengthen foundations | Pending |
| 13 | XLOOKUP fundamentals | COMPLETED — EARLIER SESSION | Completed in an earlier learning session | Completed |
| 14 | Reverse XLOOKUP and advanced lookup topics | NOT STARTED | Pending | Pending |

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

## 2026-11-14 — COUNTIF/COUNTIFS combined review and Lesson 09 completion

### Practice and assessment completed

- Completed a three-condition OR exercise using Critical priority, days overdue >300 and Failed inspection status.
- Independently calculated all three individual counts, all three pairwise overlaps and the triple overlap.
- Correctly used the three-set Inclusion–Exclusion Principle: add the individual counts, subtract each pairwise overlap, then add the triple overlap once.
- Corrected the triple-overlap term from subtraction to addition after reviewing why it must be restored; final result was 5 equipment records.
- Passed the combined five-question COUNTIF/COUNTIFS assessment (5/5):
  1. COUNTIF days overdue >200: 4.
  2. Pump AND days overdue >100: 1.
  3. Compressor AND days >100 AND days <400: 2.
  4. Pump OR days overdue >400: 3.
  5. (Compressor AND days >100) OR (Valve AND days >300): 3.
- Independently constructed the formulas for all five questions.
- Correctly explained why the triple overlap is added back: it was removed three times by the pairwise subtractions.

### Status and next action

- Lesson 09 — COUNTIF and COUNTIFS: **COMPLETED**.
- Next: begin practical SUMIF/SUMIFS with engineering-register examples. Keep VLOOKUP deferred until the lookup sequence is appropriate.

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


## 2026-11-13 — COUNTIF independent assessment

### Assessment completed and verified

Using the eight-record maintenance-age dataset, the learner independently answered all five COUNTIF questions correctly:

1. Days >180: `=COUNTIF(B2:B9,">180")` → 4.
2. Days >=180: `=COUNTIF(B2:B9,">=180")` → 5.
3. Days exactly 365: `=COUNTIF(B2:B9,"=365")` → 1.
4. Days not equal to 365: `=COUNTIF(B2:B9,"<>365")` → 7.
5. Equipment type Pump: `=COUNTIF(A2:A9,"Pump")` → 2.

Score: **5/5**. The learner also correctly explained that `>180` excludes 180 while `>=180` includes 180.

### Current status and next action

- COUNTIF single-condition assessment: passed.
- COUNTIFS multi-condition and date-range practice: verified.
- Lesson 09 remains open for one short combined COUNTIF/COUNTIFS review before completion.


## 2026-11-15 — SUMIF and SUMIFS completion

### Concepts and practice completed

- Studied SUMIF syntax and independently practised text criteria, numerical criteria, inclusive and exclusive comparisons, and cell-reference criteria.
- Practised wildcard criteria: starts with (`Pump*`), ends with (`*Pump`), contains (`*Pump*`) and single-character wildcard (`?`).
- Studied SUMIFS syntax and the difference in argument order: SUMIF starts with the criteria range; SUMIFS starts with the sum range.
- Independently practised two- and three-condition SUMIFS calculations using AND logic.
- Practised numerical thresholds and bounded ranges by applying two criteria to the maintenance-cost range.
- Used cell references and concatenation (`&`) to create dynamic numerical criteria.
- Learned that hardcoding means entering criteria directly in a formula, while cell references make criteria dynamic.
- Practised OR logic by adding separate SUMIFS calculations.
- Practised combined AND + OR logic with two multi-condition groups.
- Discussed double-counting when a record qualifies for both groups.
- Diagnosed a SUMIF result of 0.00 caused by maintenance-cost values stored as text. Converted values into numeric values in helper column D and verified the correct total.

### Independent assessment

Passed all five assessment questions (5/5):

1. Maintenance cost > ₹20,000: ₹77,000. Passed after converting text values to numbers.
2. Pump AND Critical: ₹30,000. Correct.
3. Critical AND maintenance cost > ₹15,000: ₹43,000. Correct.
4. Critical OR High: ₹1,27,000. Initially used an AND-style formula, then corrected it to two SUMIFS calculations added together.
5. (Pump AND Critical) OR (Compressor AND High): ₹60,000. Correct.

### Status and next action

- Lesson 10 — SUMIF and SUMIFS: **COMPLETED**.
- Next lesson: AVERAGEIF and AVERAGEIFS, using offshore equipment performance and maintenance datasets.
- VLOOKUP remains deferred until the lookup sequence is appropriate.


## 2026-11-16 — AVERAGEIF and AVERAGEIFS practice

### Concepts and practice completed

- Studied AVERAGEIF syntax and the roles of criteria range, criterion and average range.
- Independently wrote correct AVERAGEIF formulas for Pump equipment and Critical priority.
- Practised numeric criteria, including greater-than and greater-than-or-equal-to comparisons.
- Practised dynamic numeric criteria using concatenation, for example `">="&E6`; correctly explained why `">=E6"` is literal text rather than a dynamic reference.
- Practised wildcard criteria: begins with (`Pump*`) and contains (`*Pump*`). Correctly calculated the separate wildcard example average of ₹26,250 after aligning the formula to the actual worksheet columns.
- Studied AVERAGEIFS syntax and its argument order: average range first, followed by criteria-range/criterion pairs.
- Independently wrote correct AVERAGEIFS formulas using two and three simultaneous conditions (AND logic).
- Practised mixed text and numeric conditions, dynamic cell references, and not-equal criteria (`<>Low`).
- Practised OR logic by combining separate AVERAGEIFS groups. Learned that adding group averages does not produce the combined average; the group averages must be weighted by their record counts.
- Identified overlapping OR groups: Critical count = 4, Pump count = 4, overlap (Pump AND Critical) = 2.
- Correctly explained that overlapping records are double-counted if group totals and counts are simply added.
- Learned the two-set Inclusion–Exclusion Principle and how to apply it separately to sums and counts before calculating a combined average.
- Correct combined-average example: Critical total ₹120,000; Pump total ₹70,000; overlap total ₹45,000; unique total ₹145,000. Unique count = 4 + 4 − 2 = 6. Combined average = ₹24,166.67.
- Corrected a function-selection misunderstanding: AVERAGE does not accept criteria; use AVERAGEIF for one condition and AVERAGEIFS for multiple conditions.

### Status and next action

- Lesson 11 — AVERAGEIF and AVERAGEIFS: **IN PROGRESS**.
- Core concepts and exercises have been practised, but the learner has not yet independently completed the combined-average calculation and final assessment.
- Next session: revise the overlap calculation, complete two independent combined-average exercises, then conduct a short assessment.
- Keep the lesson open until the learner can independently complete the assessment and explain the results.


## 2026-11-19 — Lesson 11 completion: AVERAGEIF and AVERAGEIFS

### Practice and assessment completed

- Resumed combined-average practice for overlapping OR groups (Pump OR Critical).
- Correctly explained why group averages cannot simply be added or equally averaged when group sizes differ.
- Independently calculated a weighted average for groups of 5 and 3 records: ₹15,000.
- Correctly selected COUNTIFS to count the overlap and SUMIFS to sum the overlap.
- Independently constructed the combined-average formula using SUMIF, SUMIFS, COUNTIF and COUNTIFS.
- Corrected operator precedence by placing parentheses around the full numerator and denominator.
- Completed a five-question combined-average assessment: four answers fully correct on the first attempt; one answer had an arithmetic transcription/calculation error, while the method was correct and the calculation was reviewed and corrected.
- Correct final assessment result: ₹27,857.14.

### Status and next action

- Lesson 11 — AVERAGEIF and AVERAGEIFS: **COMPLETED** (2026-11-19).
- Next lesson: Lesson 12 — MAXIFS and MINIFS.
- Next session should begin with MAXIFS/MINIFS syntax and single-/multiple-condition examples using the synthetic equipment maintenance dataset.
- User paused study after completing Lesson 11; resume when they return.
