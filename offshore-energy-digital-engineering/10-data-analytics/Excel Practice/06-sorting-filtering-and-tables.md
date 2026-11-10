# Excel Fundamentals 06 — Sorting, Filtering and Excel Tables

**Training date:** 2026-11-10  
**Status:** PRACTICAL WORK PARTIALLY VERIFIED

## Concepts covered

### Sorting
Sorts records into an order, such as tag number A to Z or quantity smallest to largest. Sort the complete dataset so that values remain aligned with their records.

### Filtering
Displays only records that meet selected criteria. Filtered-out rows are hidden, not deleted.

### Excel Tables
Use Ctrl+T to convert a data range into a table. Confirm that the table has headers. Tables provide header filters, consistent formatting, structured references and expansion behaviour when new records are added directly below the table.

## Practice task

Create an equipment register with Tag Number, Equipment, Discipline and Quantity. Practise:
- Sorting Quantity smallest to largest.
- Sorting Tag Number A to Z.
- Filtering Mechanical and Instrumentation records.
- Clearing filters to show all records.
- Converting the range into a table.
- Renaming the table to `EquipmentRegister`.

## Work observed

The learner shared a screenshot showing:
- An Excel table named `Table1`.
- Quantity values sorted ascending: 2, 3, 4, 5, 6.
- Header filter controls visible.
- A structured-reference formula: `=SUM(Table1[Quantity])`.
- The total displayed with a date format, which was diagnosed and corrected conceptually in the lesson.

The screenshot verifies table creation, ascending quantity order and use of a structured reference. It does not independently verify that each filter exercise was completed.

## Structured-reference example

```excel
=SUM(Table1[Quantity])
```

This adds all values in the Quantity column of Table1.

## Next action

Practise filtering by Discipline and confirm that clearing the filter restores all rows.
