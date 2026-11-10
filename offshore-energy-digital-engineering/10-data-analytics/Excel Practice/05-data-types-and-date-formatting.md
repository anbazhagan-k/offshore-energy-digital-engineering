# Excel Fundamentals 05 — Data Types, Number Formats and Dates

**Training date:** 2026-11-10  
**Status:** STUDIED — date serial-number concept clarified

## Concepts covered

Common spreadsheet values include:
- Text: equipment descriptions and identifiers.
- Numbers: quantities, costs and measurements.
- Dates: inspection and revision dates.
- Percentages: rates and completion proportions.

Equipment tags such as `P-001` are identifiers and should generally be stored as text. This preserves leading zeros and avoids treating identifiers as quantities.

## Formatting versus stored value

Formatting changes how a value is displayed; it does not normally change the underlying value.

Examples:
- A stored value of 500 can be displayed as 500, 500.00 or currency.
- A stored value of 0.18 displayed as a percentage appears as 18%.
- A date is stored as a serial number in Excel's date system and displayed using a date format.

## Date serial numbers

In Excel's standard 1900 date system, dates are represented by sequential serial numbers. This allows date arithmetic.

Example:
```excel
=B2-A2
```
If A2 is 10-Nov-2026 and B2 is 11-Nov-2026, the result is 1 day.

## Troubleshooting task completed

The learner used `=SUM(Table1[Quantity])` to total a table column. The result displayed as `19-Jan-1900` because the result cell had a date format. The underlying calculation was 20. Changing the cell format to General or Number displays the numeric result correctly.

## Key lesson

Always distinguish the stored value from its display format. A correct formula can appear to return an unexpected result if the output cell is formatted incorrectly.
