# Lesson 12 — MAXIFS and MINIFS

**Learning environment:** Google Sheets  
**Certification alignment:** Microsoft Office Specialist: Excel Expert (Microsoft 365 Apps), MO-211  
**Status:** IN PROGRESS — core practice completed; independent assessment pending  
**Session date:** 2026-11-20

## Learning objectives

- Find maximum and minimum values that meet one or more conditions.
- Apply multiple criteria using AND logic.
- Use numeric comparison criteria.
- Build dynamic criteria using cell references and concatenation.
- Apply date criteria and inclusive date ranges.
- Combine text, numeric and date conditions in one formula.

## Dataset used

Initial synthetic maintenance dataset:

| Equipment ID (A) | Discipline (B) | Maintenance Cost (C) |
|---|---|---:|
| P-101 | Mechanical | 25,000 |
| M-102 | Mechanical | 18,000 |
| E-103 | Electrical | 12,000 |
| P-104 | Mechanical | 32,000 |
| E-105 | Electrical | 15,000 |
| I-106 | Instrumentation | 8,000 |
| M-107 | Mechanical | 21,000 |
| E-108 | Electrical | 19,000 |
| I-109 | Instrumentation | 11,000 |
| P-110 | Mechanical | 28,000 |

A later date-based exercise introduced column D as Maintenance Date and used a stated practice range of rows 2–20. The date-based exercises were formula-writing exercises; no underlying date dataset or calculated outputs were supplied in the session.

## 1. Syntax

`=MAXIFS(max_range, criteria_range1, criterion1, ...)`

`=MINIFS(min_range, criteria_range1, criterion1, ...)`

- `max_range` / `min_range`: values from which the highest or lowest qualifying value is returned.
- Each `criteria_range` is checked against its corresponding criterion.
- All criteria pairs must be satisfied (AND logic).

## 2. Single-condition practice

Highest Mechanical maintenance cost:

```excel
=MAXIFS(C2:C11,B2:B11,"Mechanical")
```

Expected result: ₹32,000.

Lowest Electrical maintenance cost:

```excel
=MINIFS(C2:C11,B2:B11,"Electrical")
```

Expected result: ₹12,000.

Both formulas were independently written correctly by the learner.

## 3. Multiple conditions and numeric criteria

Highest Mechanical maintenance cost greater than ₹20,000:

```excel
=MAXIFS(C2:C11,B2:B11,"Mechanical",C2:C11,">20000")
```

Expected result: ₹32,000.

Lowest Mechanical maintenance cost greater than ₹20,000:

```excel
=MINIFS(C2:C11,B2:B11,"Mechanical",C2:C11,">20000")
```

Expected result: ₹21,000.

The learner correctly used the cost range as both the value range and a criteria range to apply the numeric threshold.

## 4. Dynamic cell-reference criteria

If E2 contains the discipline and F2 contains the numeric threshold, use:

```excel
=MAXIFS(C2:C11,B2:B11,E2,C2:C11,">"&F2)
```

For the minimum:

```excel
=MINIFS(C2:C11,B2:B11,E2,C2:C11,">"&F2)
```

The learner independently wrote both formula patterns correctly. In one response the learner used E3 and F3 rather than the exercise's E2 and F2; the formula structure was correct if the input values were actually located in row 3.

The expression `">"&F2` joins the comparison operator to the value in F2 to create a dynamic criterion such as `">20000"`.

## 5. Date-based criteria

Use `DATE(year,month,day)` to construct a date criterion safely.

After 1 January 2026, for Mechanical equipment:

```excel
=MAXIFS(C2:C20,B2:B20,"Mechanical",D2:D20,">"&DATE(2026,1,1))
```

The learner initially attempted to write the date as `1-1-2026`, which is interpreted as arithmetic rather than a date value. The learner then correctly used the DATE function in subsequent exercises.

For a date range inclusive of 1 January through 31 March 2026:

```excel
=MAXIFS(C2:C11,B2:B11,"Mechanical",D2:D11,">="&DATE(2026,1,1),D2:D11,"<="&DATE(2026,3,31))
```

For an inclusive date range, use both a lower-bound criterion (`>=`) and an upper-bound criterion (`<=`) on the date column.

Useful date criteria:

| Requirement | Criterion |
|---|---|
| After a date | `">"&DATE(2026,1,1)` |
| Before a date | `"<"&DATE(2026,1,1)` |
| On or after | `">="&DATE(2026,1,1)` |
| On or before | `"<="&DATE(2026,1,1)` |

**Range consistency:** Every criteria range must cover the same corresponding rows as the maximum/minimum range. The session included both rows 2–11 and a later stated exercise range of rows 2–20; match the range to the actual dataset in the worksheet.

## 6. Combined text, numeric and date conditions

Highest Electrical maintenance cost greater than ₹10,000, between 1 January and 30 June 2026 inclusive:

```excel
=MAXIFS(C2:C20,B2:B20,"Electrical",C2:C20,">10000",D2:D20,">="&DATE(2026,1,1),D2:D20,"<="&DATE(2026,6,30))
```

The learner independently wrote this formula correctly, combining four criteria:
1. Discipline = Electrical.
2. Maintenance cost > ₹10,000.
3. Maintenance date >= 1 January 2026.
4. Maintenance date <= 30 June 2026.

## Session evidence — 2026-11-20

The learner independently supplied correct formula structures for:
- MINIFS with one text condition.
- MAXIFS with a text condition and numeric threshold.
- MINIFS with a text condition and numeric threshold.
- MAXIFS with dynamic text and numeric cell references.
- MINIFS with dynamic text and numeric cell references.
- MAXIFS with a date condition using DATE().
- MINIFS with a date condition using DATE(); the learner used 2 January rather than the originally requested 1 January, and the corrected date was discussed.
- MAXIFS with an inclusive date range and a discipline condition.
- MINIFS with an inclusive half-year date range and a discipline condition.
- MAXIFS combining a discipline, numeric threshold and inclusive date range.

The learner correctly explained/used AND logic through multiple criteria pairs. The formulas were checked for structure. Date-based formula outputs were not verified against an actual date dataset in this session.

## Assessment and completion status

- Core concepts and guided/independent formula practice: **PRACTISED**.
- Independent five-question assessment: **PENDING**. The assessment was introduced but the learner had not yet answered Question 1 at the time of this update.
- Lesson status: **IN PROGRESS**. Do not mark COMPLETED until the learner passes the independent assessment and the results are checked.

## Next action

Resume with the five-question independent MAXIFS/MINIFS assessment. Begin with the maximum maintenance cost for Instrumentation equipment, using rows 2–20.
