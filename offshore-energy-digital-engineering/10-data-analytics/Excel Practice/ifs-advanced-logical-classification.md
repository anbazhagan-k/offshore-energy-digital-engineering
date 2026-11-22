# Supplementary Practice — IFS and Advanced Logical Classification

**Learning environment:** Google Sheets; formulas are compatible with Excel 365  
**Career context:** Synthetic offshore asset maintenance and engineering information data  
**Status:** IN PROGRESS  
**Started:** 2026-11-21

## Purpose

Build deeper understanding of IFS before moving to SWITCH. Focus on condition order, first-TRUE evaluation, boundary values, fallback conditions, missing values, and nested AND/OR logic.

## Dataset

The companion workbook is:

[offshore_asset_maintenance_ifs_practice.xlsx](ifs-practice/offshore_asset_maintenance_ifs_practice.xlsx)

It contains 30 synthetic equipment records and an IFS Practice Guide worksheet. The asset maintenance data fields are:

| Column | Field |
|---|---|
| A | Asset ID |
| B | Equipment Name |
| C | Discipline |
| D | Location |
| E | Maintenance Cost (INR) |
| F | Downtime (Hours) |
| G | Inspection Score |
| H | Last Maintenance Date |
| I | Work Order Status |

The dataset is synthetic and intended only for learning. Do not use employer-confidential or proprietary data.

## Concepts practised

### 1. IFS syntax and multiple classifications

`=IFS(condition1,result1,condition2,result2,...)`

IFS evaluates conditions from left to right and returns the result associated with the first condition that evaluates to TRUE.

Example:

```excel
=IFS(E2>150000,"Very Critical",E2>100000,"Critical",E2>60000,"High",E2>30000,"Medium",E2<=30000,"Low")
```

### 2. Boundary values

The learner tested exact thresholds and correctly classified:

| Cost | Category |
|---:|---|
| ₹150,000 | Critical |
| ₹100,000 | High |
| ₹60,000 | Medium |
| ₹30,000 | Low |

This reinforced the difference between `>` and `>=`.

### 3. Condition order and first-TRUE behaviour

A deliberately misordered formula placed `E2>30000` before higher thresholds. With E2 = ₹160,000, the first condition was TRUE, so IFS returned "Medium" without evaluating later conditions.

### 4. Fallback condition and #N/A

If no condition is TRUE and no fallback is supplied, IFS returns `#N/A`. A final `TRUE,"Low"` pair provides a default result.

### 5. Blank and zero handling

The learner independently wrote:

```excel
=IFS(E2="","Not Available",E2=0,"No Maintenance Cost",E2>100000,"Critical",E2>50000,"High",E2>20000,"Medium",TRUE,"Low")
```

Blank and zero checks are placed before numeric bands.

### 6. AND and OR inside IFS

The learner practised multiple conditions for a single result:

```excel
=IFS(AND(E2>100000,F2>100),"Critical",OR(E2>75000,G2<50),"High",F2>50,"Medium",TRUE,"Low")
```

Key distinction:
- `AND()`: every included logical test must be TRUE.
- `OR()`: at least one included logical test must be TRUE.

### 7. Nested AND/OR logic

The learner independently constructed:

```excel
=IFS(AND(E2>150000,OR(F2>100,G2<40)),"Critical",AND(E2>100000,F2>60),"High",OR(E2>50000,F2>50),"Medium",TRUE,"Low")
```

Critical requires cost above ₹150,000 AND at least one of downtime above 100 or inspection score below 40.

A further scenario introduced a nested High condition:

```excel
AND(OR(E2>100000,F2>80),G2<70)
```

The learner initially reused the prior High condition, then reviewed the required OR group and inspection-score condition. A test record with cost ₹90,000, downtime 90 and score 65 was correctly identified as High after tracing the formula.

## Practice evidence and corrections

- Correctly wrote four-band and five-band IFS classifications.
- Correctly handled downtime boundaries after correcting strict comparisons at 60 and 30 hours.
- Correctly used a final TRUE fallback.
- Correctly checked blank and zero before numeric conditions.
- Correctly explained why IFS stops at the first TRUE condition.
- Correctly identified #N/A when no condition matched and no fallback existed.
- Correctly explained why Asset E was High rather than Critical when the Critical AND condition failed but the High OR condition succeeded.
- In one asset classification exercise, two answers were corrected after tracing each condition: Asset A was Critical, Asset C was Medium and Asset D was Low. This reinforced evaluating the formula in order rather than judging from one data field.

## Current advanced exercise

### Exercise 9 — nested classification across three fields

**Formula construction: PASSED (2026-11-22).** The learner independently submitted the correct IFS formula with all four classification bands and the correct condition order:

```excel
=IFS(AND(E2>150000,OR(F2>100,G2<40)),"Critical",AND(OR(E2>100000,F2>80),G2<70),"High",OR(AND(E2>50000,G2<80),F2>60),"Medium",TRUE,"Low")
```

The formula matches the required rules. The learner corrected the Medium condition after feedback, changing it to `(cost > ₹50,000 AND inspection score <80) OR downtime >60`.

**Record-level testing remains pending.** The learner must test the formula against multiple workbook records and trace why each result is returned.

Exercise 9 requirements:

- Critical: cost > ₹150,000 AND (downtime > 100 OR score < 40).
- High: (cost > ₹100,000 OR downtime > 80) AND score < 70.
- Medium: (cost > ₹50,000 AND score < 80) OR downtime > 60.
- Low: otherwise.

The learner must independently construct the full IFS formula and test it against multiple records.

## Exercise 9 — record-level validation

**Record-level testing: PASSED (2026-11-22).** The learner tested the formula against five workbook records using Maintenance Cost, Downtime and Inspection Score. All five classifications matched the expected results: Medium, Medium, Low, Medium and Low. The second record was correctly classified Medium because downtime exceeded 60 hours, even though it did not qualify as High.

## Exercise 11 — status-aware IFS classification

**Formula construction: PASSED (2026-11-22).** The learner independently constructed a status-aware IFS formula using Work Order Status (I), Maintenance Cost (E), Downtime (F) and Inspection Score (G). The six ordered rules were: Closed → Completed; In Progress with cost > ₹100,000 OR downtime >80 OR score <50 → Escalate; Open with score <60 → Inspection Required; remaining In Progress → In Progress; remaining Open → Awaiting Action; otherwise → Review Status. The learner initially mistyped `TRUE` as `TURE` and corrected it after feedback.

**Manual validation: PASSED (5/5).** The learner correctly predicted the first five records as In Progress, Awaiting Action, Completed, In Progress and Completed. The learner demonstrated understanding of rule priority and fallback behaviour.

## Remaining work

1. Practise date-based maintenance-cycle and overdue classification.
2. Test blank, zero, text and invalid-value cases.
3. Complete an independent IFS assessment before marking this supplementary practice complete.
4. Only then proceed to SWITCH.
3. Practise date-based maintenance-cycle and overdue classification.
4. Test blank, zero, text and invalid-value cases.
5. Complete an independent IFS assessment before marking this supplementary practice complete.
6. Only then proceed to SWITCH.

## Completion rule

Do not mark this practice complete until the learner can explain condition order, construct nested logic independently, test boundary cases and pass a short assessment.
