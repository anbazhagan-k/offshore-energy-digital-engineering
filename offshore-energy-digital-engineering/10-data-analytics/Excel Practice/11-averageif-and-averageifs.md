# Lesson 11 — AVERAGEIF and AVERAGEIFS

**Learning environment:** Google Sheets  
**Certification alignment:** Microsoft Office Specialist: Excel Expert (Microsoft 365 Apps), MO-211  
**Status:** COMPLETED — independent combined-average assessment passed (4/5 fully correct on first attempt; one arithmetic correction reviewed)  
**Session date:** 2026-11-16

## Learning objectives

- Calculate averages using one or more criteria.
- Apply text, numeric, comparison-operator and wildcard criteria.
- Build dynamic criteria using cell references and concatenation.
- Combine AND and OR logic.
- Avoid double-counting when criteria groups overlap.
- Calculate a correct combined average from overlapping groups.

## Dataset used

The learner practised with a synthetic maintenance dataset:

| Equipment (A) | Maintenance cost (B) | Priority (C) | Discipline (D) |
|---|---:|---|---|
| Pump | 20,000 | Critical | Mechanical |
| Compressor | 30,000 | High | Mechanical |
| Pump | 15,000 | High | Electrical |
| Generator | 40,000 | Critical | Electrical |
| Pump | 25,000 | Critical | Mechanical |
| Compressor | 35,000 | Critical | Mechanical |
| Generator | 20,000 | High | Electrical |
| Pump | 10,000 | Low | Mechanical |

A separate wildcard example used rows 12–17, with equipment in column A and cost in column C.

## 1. AVERAGEIF — one condition

Syntax:

`=AVERAGEIF(criteria_range, criterion, [average_range])`

- `criteria_range`: cells checked against the condition.
- `criterion`: condition to match.
- `average_range`: numeric cells to average.

Examples:

```excel
=AVERAGEIF(A2:A9,"Pump",B2:B9)
```

Result: ₹17,500 (four Pump records).

```excel
=AVERAGEIF(B2:B9,">20000",B2:B9)
```

Result: ₹32,500 (values strictly greater than ₹20,000).

Comparison criteria covered: `>`, `>=`, `<`, `<=`, `<>`.

### Dynamic numeric criteria

If E6 contains 20000:

```excel
=AVERAGEIF(B2:B9,">"&E6,B2:B9)
=AVERAGEIF(B2:B9,">="&E6,B2:B9)
```

The operator is concatenated with the cell reference using `&`. The expression `">=E6"` is literal text, whereas `">="&E6` constructs a criterion using the value in E6.

### Wildcards

- `"Pump*"`: begins with Pump.
- `"*Pump"`: ends with Pump.
- `"*Pump*"`: contains Pump anywhere.
- `"P?mp"`: exactly one character at the question-mark position.
- `~` can escape a wildcard character when it should be treated literally.

Example for the separate rows 12–17 dataset:

```excel
=AVERAGEIF(A12:A17,"*Pump*",C12:C17)
```

Matching costs: 20,000, 30,000, 40,000 and 15,000. Result: ₹26,250.

**Worksheet layout correction:** The first dataset used A = Equipment and B = Maintenance Cost. A later separate wildcard dataset used A = Equipment and C = Maintenance Cost. Always check the actual worksheet columns before writing a formula.

## 2. AVERAGEIFS — multiple conditions

Syntax:

`=AVERAGEIFS(average_range, criteria_range1, criterion1, [criteria_range2, criterion2], ...)`

Important difference: AVERAGEIFS starts with the average range, unlike AVERAGEIF.

Two conditions (AND):

```excel
=AVERAGEIFS(B2:B9,A2:A9,"Compressor",C2:C9,"Critical")
```

Result: ₹35,000.

Three conditions (AND):

```excel
=AVERAGEIFS(B2:B9,A2:A9,"Pump",C2:C9,"Critical",D2:D9,"Mechanical")
```

Result: ₹22,500.

Numeric condition and text condition:

```excel
=AVERAGEIFS(B2:B9,C2:C9,"Critical",B2:B9,">20000")
```

Result: ₹33,333.33.

Dynamic criteria using E5 = 20000, F5 = Pump and G5 = Critical:

```excel
=AVERAGEIFS(B2:B9,B2:B9,">="&E5,A2:A9,F5,C2:C9,G5)
```

Result: ₹22,500.

For a not-equal condition, use `"<>Low"`. Example:

```excel
=AVERAGEIFS(B2:B9,A2:A9,"Pump",C2:C9,"<>Low",B2:B9,">=15000")
```

Result: ₹20,000.

## 3. AND and OR logic

AVERAGEIFS applies AND logic between its criteria pairs. To express OR logic, calculate the groups separately.

Example:

- Pump AND Critical: costs 20,000 and 25,000; group average = ₹22,500.
- Compressor AND High: cost 30,000; group average = ₹30,000.

Adding the two group averages is **not** the combined average. The combined average must be weighted by the number of records in each group:

```excel
=(AVERAGEIFS(B2:B9,A2:A9,"Pump",C2:C9,"Critical")*COUNTIFS(A2:A9,"Pump",C2:C9,"Critical")
 +AVERAGEIFS(B2:B9,A2:A9,"Compressor",C2:C9,"High")*COUNTIFS(A2:A9,"Compressor",C2:C9,"High"))
 /(COUNTIFS(A2:A9,"Pump",C2:C9,"Critical")+COUNTIFS(A2:A9,"Compressor",C2:C9,"High"))
```

Result: ₹25,000.

## 4. Overlapping OR groups and double-counting

For:

- Group A: Priority = Critical
- Group B: Equipment = Pump

The learner correctly identified the overlap: Pump records that are also Critical satisfy both groups.

Counts:
- Critical: 4
- Pump: 4
- Both Critical AND Pump: 2

Unique records satisfying either condition:

`4 + 4 - 2 = 6`

This is the two-set Inclusion–Exclusion Principle:

`A ∪ B = A + B − (A ∩ B)`

The same principle must be applied separately to totals and counts when calculating an average.

For this dataset:
- Critical total = ₹130,000? **Check carefully:** 20,000 + 40,000 + 25,000 + 35,000 = ₹120,000.
- Pump total = ₹70,000.
- Overlap total (Pump AND Critical) = ₹45,000.
- Combined total = ₹120,000 + ₹70,000 − ₹45,000 = ₹145,000.
- Combined count = 4 + 4 − 2 = 6.
- Combined average = ₹145,000 ÷ 6 = **₹24,166.67**.

Correct Google Sheets formula:

```excel
=(SUMIF(C2:C9,"Critical",B2:B9)
 +SUMIF(A2:A9,"Pump",B2:B9)
 -SUMIFS(B2:B9,C2:C9,"Critical",A2:A9,"Pump"))
 /(COUNTIF(C2:C9,"Critical")
 +COUNTIF(A2:A9,"Pump")
 -COUNTIFS(C2:C9,"Critical",A2:A9,"Pump"))
```

**Important:** Subtracting the overlap average from the two group averages is incorrect. Inclusion–Exclusion must be applied to the underlying sum and count, then divide the combined sum by the combined count.

## 5. Function selection

| Function | Use |
|---|---|
| AVERAGE | Average numeric values without a condition |
| AVERAGEIF | Average values meeting one condition |
| AVERAGEIFS | Average values meeting multiple AND conditions |
| SUMIF / SUMIFS | Sum values meeting one or multiple conditions |
| COUNTIF / COUNTIFS | Count records meeting one or multiple conditions |

## Session evidence — 2026-11-16

The learner independently:
- Wrote correct AVERAGEIF formulas for Pump, Critical, numeric thresholds, dynamic criteria and wildcard matching.
- Correctly used AVERAGEIFS with two and three conditions.
- Corrected a `Low` criterion to `<>Low` after identifying the task's "not Low" requirement.
- Explained why dynamic numeric criteria need concatenation (`">="&E5`) while text criteria can use a direct cell reference (F5 or G5).
- Built OR logic using separate AVERAGEIFS groups and learned why simply adding averages is incorrect.
- Correctly identified overlapping counts (4 Critical, 4 Pump, 2 in both).
- Explained the double-counting issue and learned the Inclusion–Exclusion Principle.
- Was shown how to calculate the combined average using deduplicated totals and counts.

## Assessment and completion — 2026-11-19

The learner resumed the lesson and independently worked through the combined-average problem for overlapping OR groups (Equipment = Pump OR Priority = Critical).

### Concepts verified

- Explained why simply averaging two group averages is not generally correct: groups with different record counts need different weights.
- Correctly calculated weighted averages for groups of 5 and 3 records, obtaining ₹15,000.
- Identified `COUNTIFS` as the function to count the intersection (Pump AND Critical).
- Identified `SUMIFS` as the function to sum the intersection cost.
- Independently constructed the combined-average formula using `SUMIF`, `SUMIFS`, `COUNTIF` and `COUNTIFS`.
- Corrected the formula's operator-precedence issue by enclosing the complete numerator and denominator in parentheses.
- Independently calculated the combined average in the final assessment as ₹27,857.14.

### Independent assessment record

Five assessment questions were attempted:

1. Correct: ₹24,285.71.
2. Correct method, but arithmetic inputs were transcribed incorrectly in the first calculation. Reviewed and corrected to ₹32,000.
3. Correct: ₹30,000.
4. Correct complete Excel formula for Compressor OR High, with overlap removed.
5. Correct: ₹27,857.14.

**Assessment outcome:** 4/5 fully correct on first attempt; one arithmetic correction was needed and reviewed. The learner demonstrated the combined-average method and independently produced the final correct calculation and formula structure. Lesson marked **COMPLETED**.

## Status

**COMPLETED — 2026-11-19.** Core AVERAGEIF/AVERAGEIFS concepts, dynamic and wildcard criteria, AND/OR logic, weighted averages and overlap removal have been practised and assessed.
