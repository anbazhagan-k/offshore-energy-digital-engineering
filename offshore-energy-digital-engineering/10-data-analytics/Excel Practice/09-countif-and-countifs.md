# Excel Lesson 09 — COUNTIF and COUNTIFS

**Study date:** 2026-11-12  
**Status:** STUDIED — independent practice and assessment still required  
**Application:** Counting equipment types, maintenance priorities and overdue assets in engineering registers.

## Learning objectives

- Explain the difference between COUNTIF and COUNTIFS.
- Count cells matching one text or numerical condition.
- Use comparison operators in COUNTIF.
- Count records matching two or more conditions with COUNTIFS.
- Combine text criteria and numerical criteria.
- Check boundary values and verify results independently.

## 1. COUNTIF — one condition

COUNTIF counts cells in a range that meet one condition.

**Syntax**

```excel
=COUNTIF(range, criteria)
```

- `range`: cells Excel should examine.
- `criteria`: the condition Excel should match.

Example: count Critical values in C2:C11.

```excel
=COUNTIF(C2:C11,"Critical")
```

Example: count Pumps in B2:B11.

```excel
=COUNTIF(B2:B11,"Pump")
```

Text criteria are enclosed in quotation marks.

## 2. COUNTIF with numerical conditions

Comparison operators:

| Operator | Meaning |
|---|---|
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `=` | Equal to |
| `<>` | Not equal to |

Example: count equipment items with at least 180 maintenance days.

```excel
=COUNTIF(B2:B9,">=180")
```

The criteria string, including the operator and number, must be enclosed in quotation marks. For example, `">=180"` is valid; `>=180` without quotation marks is not valid as a COUNTIF criteria argument.

### Demonstration dataset

| Equipment | Days since maintenance |
|---|---:|
| P-101 | 45 |
| P-102 | 90 |
| C-101 | 150 |
| C-102 | 180 |
| V-101 | 250 |
| V-102 | 365 |
| E-101 | 400 |
| E-102 | 500 |

Examples:
- `=COUNTIF(B2:B9,">=180")` → 5
- `=COUNTIF(B2:B9,">180")` → 4
- `=COUNTIF(B2:B9,"<=150")` → 3
- `=COUNTIF(B2:B9,"<>365")` → 7

The difference between `>180` and `>=180` is important: the first excludes exactly 180; the second includes it.

## 3. COUNTIFS — multiple conditions

COUNTIFS counts records only when all supplied criteria pairs are satisfied. It applies AND logic between criteria pairs.

**Syntax**

```excel
=COUNTIFS(criteria_range1, criteria1, criteria_range2, criteria2, ...)
```

Each criteria range must correspond to the range containing the condition to test. In normal register work, all criteria ranges should have matching dimensions.

Example equipment dataset:

| Equipment ID | Type (B) | Days (C) | Priority (D) |
|---|---|---:|---|
| P-101 | Pump | 400 | Critical |
| P-102 | Pump | 120 | High |
| P-103 | Pump | 250 | Medium |
| C-101 | Compressor | 365 | Critical |
| C-102 | Compressor | 90 | Low |
| V-101 | Valve | 180 | High |
| V-102 | Valve | 450 | Critical |
| E-101 | Exchanger | 200 | Medium |
| E-102 | Exchanger | 60 | Low |
| C-103 | Compressor | 300 | High |

### Example A — Critical Pumps

```excel
=COUNTIFS(B2:B11,"Pump",D2:D11,"Critical")
```

Expected result: **1**. Only P-101 meets both conditions.

### Example B — Critical Compressors

```excel
=COUNTIFS(B2:B11,"Compressor",D2:D11,"Critical")
```

Expected result: **1**. Only C-101 meets both conditions.

### Example C — Critical equipment with 180 days or more

```excel
=COUNTIFS(D2:D11,"Critical",C2:C11,">=180")
```

Expected result: **3** — P-101, C-101 and V-102.

## 4. COUNTIFS practice — pending learner assessment

Use the ten-record equipment dataset in Section 3. The learner has been shown these practice questions and formulas, but has not yet submitted independent answers. Do not mark them complete until attempted and checked.

| No. | Question | Formula | Expected count |
|---:|---|---|---:|
| 1 | How many Compressors have Critical priority? | `=COUNTIFS(B2:B11,"Compressor",D2:D11,"Critical")` | 1 |
| 2 | How many Valves have Critical priority? | `=COUNTIFS(B2:B11,"Valve",D2:D11,"Critical")` | 1 |
| 3 | How many Pumps have High priority? | `=COUNTIFS(B2:B11,"Pump",D2:D11,"High")` | 1 |
| 4 | How many High-priority items have more than 180 maintenance days? | `=COUNTIFS(D2:D11,"High",C2:C11,">180")` | 1 |
| 5 | How many Critical items have fewer than 365 maintenance days? | `=COUNTIFS(D2:D11,"Critical",C2:C11,"<365")` | 0 |
| 6 | How many Pumps have at least 200 maintenance days? | `=COUNTIFS(B2:B11,"Pump",C2:C11,">=200")` | 2 |

## 5. Common errors to avoid

1. **Mismatched range sizes:** criteria ranges should cover corresponding rows. Avoid using B2:B11 with D2:D10.
2. **Missing quotation marks:** text criteria such as `"Pump"` and comparison criteria such as `">=180"` need quotation marks.
3. **Wrong boundary operator:** `>180` excludes 180; `>=180` includes 180.
4. **Misunderstanding COUNTIFS:** all criteria pairs must be satisfied. COUNTIFS uses AND logic, not OR logic.
5. **Counting the wrong field:** use the Type column for equipment type, Priority for priority, and Days for maintenance age.

## 6. Learning status

- COUNTIF syntax and text criteria: studied through examples.
- COUNTIF numerical criteria and comparison operators: studied through examples.
- COUNTIFS syntax and multiple text criteria: studied through examples.
- COUNTIFS with text and numerical criteria: studied through examples.
- Independent COUNTIF assessment: not yet recorded.
- Independent COUNTIFS assessment: pending; questions are listed in Section 4.

## Next lesson

Complete the pending COUNTIFS questions independently. Then learn three or more criteria, date ranges and practical document-register reporting. Do not move to SUMIF/SUMIFS until COUNTIF and COUNTIFS are understood and practised.
