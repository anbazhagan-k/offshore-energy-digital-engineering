# Excel Lesson 09 — COUNTIF and COUNTIFS

**Study dates:** 2026-11-12 to 2026-11-13  
**Status:** COUNTIF AND COUNTIFS PRACTISED — COMBINED REVIEW PENDING  
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

## 4. COUNTIFS practice — completed learner practice

Use the ten-record equipment dataset in Section 3. The learner independently supplied the formulas and correct counts for all six exercises. All six were checked successfully.

| No. | Question | Formula | Expected count |
|---:|---|---|---:|
| 1 | How many Compressors have Critical priority? | `=COUNTIFS(B2:B11,"Compressor",D2:D11,"Critical")` | 1 |
| 2 | How many Valves have Critical priority? | `=COUNTIFS(B2:B11,"Valve",D2:D11,"Critical")` | 1 |
| 3 | How many Pumps have High priority? | `=COUNTIFS(B2:B11,"Pump",D2:D11,"High")` | 1 |
| 4 | How many High-priority items have more than 180 maintenance days? | `=COUNTIFS(D2:D11,"High",C2:C11,">180")` | 1 |
| 5 | How many Critical items have fewer than 365 maintenance days? | `=COUNTIFS(D2:D11,"Critical",C2:C11,"<365")` | 0 |
| 6 | How many Pumps have at least 200 maintenance days? | `=COUNTIFS(B2:B11,"Pump",C2:C11,">=200")` | 2 |

### Verified results

| No. | Learner formula / task | Verified result |
|---:|---|---:|
| 1 | Compressor + Critical | 1 — correct |
| 2 | Valve + Critical | 1 — correct |
| 3 | Pump + High | 1 — correct |
| 4 | High priority + days >180 | 1 — correct |
| 5 | Critical + days <365 | 0 — correct |
| 6 | Pump + days >=200 | 2 — correct |
| 7 | Pump + Critical + days >300 | 1 — correct |
| 8 | Compressor + High + days >=300 | 1 — correct |
| 9 | Valve + High + days <=180 | 1 — correct |

## 5. Date-range counting with COUNTIFS

A date range can be counted by applying two criteria to the same date column: one lower boundary and one upper boundary.

Practice dataset (columns A:C, rows 2:9):

| Inspection ID | Equipment (B) | Inspection Date (C) |
|---|---|---|
| INS-001 | Pump | 05-Jan-2026 |
| INS-002 | Compressor | 15-Feb-2026 |
| INS-003 | Valve | 10-Mar-2026 |
| INS-004 | Pump | 20-Mar-2026 |
| INS-005 | Compressor | 05-Apr-2026 |
| INS-006 | Valve | 18-Apr-2026 |
| INS-007 | Pump | 25-May-2026 |
| INS-008 | Compressor | 10-Jun-2026 |

### March and April 2026

```excel
=COUNTIFS(C2:C9,">=01-Mar-2026",C2:C9,"<=30-Apr-2026")
```

Result: **4** — INS-003, INS-004, INS-005 and INS-006.

### April and May 2026

```excel
=COUNTIFS(C2:C9,">=01-Apr-2026",C2:C9,"<=31-May-2026")
```

Result: **3** — INS-005, INS-006 and INS-007.

### March 2026 only

```excel
=COUNTIFS(C2:C9,">=01-Mar-2026",C2:C9,"<=31-Mar-2026")
```

Result: **2** — INS-003 and INS-004.

### Pump inspections during March and April 2026

```excel
=COUNTIFS(C2:C9,">=01-Mar-2026",C2:C9,"<=30-Apr-2026",B2:B9,"Pump")
```

Result: **1** — INS-004.

### More robust date criteria using DATE and concatenation

Excel date criteria can also be constructed with `DATE()` and `&`:

```excel
=COUNTIFS(C2:C9,">="&DATE(2026,3,1),C2:C9,"<="&DATE(2026,4,30))
```

`&` joins the comparison operator text (such as `>=`) to the date value returned by `DATE()`, forming a criterion Excel can evaluate. This avoids relying on a typed date string's regional interpretation.

**Practical note:** If date cells also contain times, an inclusive criterion such as `<=31-May-2026` may exclude records later than midnight on 31 May. For date-time data, use an exclusive upper boundary such as `<1-Jun-2026` (constructed with `DATE(2026,6,1)`) to include all times on 31 May.

## 6. Common errors to avoid

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
- COUNTIFS two-condition exercises: 6/6 correct.
- COUNTIFS three-condition exercises: 3/3 correct.
- COUNTIFS date-range exercises: 4/4 correct, including a three-condition equipment/date task.
- Knowledge check: correctly identified that COUNTIFS requires all criteria to be satisfied (AND logic).
- COUNTIF independent assessment: 5/5 correct.
- COUNTIF boundary-operator knowledge check: correct; distinguished `>180` (excludes 180) from `>=180` (includes 180).

## Next lesson

Next: complete a short combined COUNTIF/COUNTIFS assessment. Single-condition COUNTIF assessment and COUNTIFS multi-condition/date-range practice have been verified. Keep the lesson open until the combined review is passed. Do not move to SUMIF/SUMIFS yet.
