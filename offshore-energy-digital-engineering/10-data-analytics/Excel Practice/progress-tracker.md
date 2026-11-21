# Excel Practice — Progress Tracker

**Last updated:** 2026-11-21  
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
| 09 | COUNTIF and COUNTIFS | COMPLETED | Single, multiple, date-range and OR criteria practised; inclusion–exclusion knowledge check passed | Assessment 5/5 |
| 10 | SUMIF and SUMIFS | COMPLETED | Text, numeric, wildcard, dynamic, AND/OR and overlap handling practised | Assessment 5/5 |
| 11 | AVERAGEIF and AVERAGEIFS | COMPLETED | Criteria, wildcards, dynamic references, AND/OR, weighted averages and overlap removal practised | Assessment 4/5 fully correct first attempt; one arithmetic correction reviewed |
| 12 | MAXIFS and MINIFS | COMPLETED (2026-11-21) | Single/multiple criteria, numeric thresholds, dynamic references, DATE() criteria and inclusive date ranges practised | Independent assessment 5/5 after one dynamic-reference correction |
| 13 | VLOOKUP fundamentals | DEFERRED | Introduced previously; paused to strengthen foundations | Pending |
| 14 | XLOOKUP fundamentals | COMPLETED — EARLIER SESSION | Completed in an earlier learning session | Completed |
| 15 | Reverse XLOOKUP and advanced lookup topics | NOT STARTED | Pending | Pending |

## 2026-11-21 — MAXIFS/MINIFS assessment and IFS advanced practice

### Lesson 12 — MAXIFS and MINIFS completion

- Completed the five-question independent assessment.
- Correctly wrote formulas for maximum Instrumentation maintenance cost, minimum Mechanical maintenance cost above ₹15,000, maximum Electrical cost during January 2026, and minimum Instrumentation cost above ₹20,000 during January 2026.
- Final question combined Mechanical discipline, January date bounds and a dynamic minimum threshold in F2.
- Initially wrote the criterion as `">F2"`; corrected it to `">"&F2` after feedback.
- Assessment result: **5/5 after correction**.
- Formula structures were validated; no supplied assessment dataset was available to verify actual returned values.
- Lesson 12 marked **COMPLETED**.

### Supplementary IFS and advanced logical classification — IN PROGRESS

A synthetic workbook with 30 offshore asset maintenance records was created and added to the repository under `ifs-practice/`. It contains asset IDs, equipment names, disciplines, locations, maintenance costs, downtime hours, inspection scores, maintenance dates and work-order statuses, plus an IFS Practice Guide worksheet.

Concepts practised:
- IFS syntax, multiple classification bands and left-to-right first-TRUE evaluation.
- Boundary values and strict versus inclusive comparisons.
- Misordered conditions and why the first TRUE condition wins.
- Final `TRUE` as a fallback; `#N/A` when no condition matches and no fallback exists.
- Blank and zero handling before numeric bands.
- AND and OR as condition expressions inside IFS.
- Nested AND/OR structures across maintenance cost, downtime and inspection score.

Learner evidence:
- Independently wrote correct five-band cost classification.
- Correctly classified boundary values ₹150,000, ₹100,000, ₹60,000 and ₹30,000.
- Explained why a misordered formula returns the first matching category.
- Correctly identified #N/A when no condition matches and no fallback exists.
- Independently wrote blank/zero handling and a combined AND/OR classification.
- Independently constructed nested Critical logic: cost > ₹150,000 AND (downtime >100 OR score <40).
- Practised a nested High condition: (cost > ₹100,000 OR downtime >80) AND score <70.
- Corrected classification mistakes by tracing each IFS condition in order.

Current assigned task: Exercise 9 — combine three logical groups, including a Medium condition of (cost > ₹50,000 AND score <80) OR downtime >60. The learner has not yet submitted the formula.

**Status:** Supplementary IFS practice remains **IN PROGRESS**. Do not move to SWITCH or mark complete until additional text/status and date-based classification practice and an independent assessment are completed.

### Next actions

1. Complete IFS Exercise 9 with nested conditions across three fields.
2. Practise status-aware and date-based IFS classification using the companion workbook.
3. Complete an independent IFS assessment.
4. Then begin SWITCH.
5. Separately, return to the additional maintenance-risk Nested IF exercise and finish filtering by Discipline in the Excel Table.
