# Lesson 01 — VLOOKUP Fundamentals

**Status:** IN PROGRESS

## Learning objective

Use VLOOKUP to search for a value in the first column of a table and return a related value from a column to its right.

## 1. What VLOOKUP does

VLOOKUP means Vertical Lookup. It searches down the first column of a selected table range. When it finds the lookup value, it returns a value from another column in the same row.

## 2. Sample equipment register

Enter this data in cells A1:C6:

| Tag Number | Equipment Description | Equipment Type |
|---|---|---|
| P-101 | Centrifugal Pump | Rotating |
| C-201 | Gas Compressor | Rotating |
| V-301 | Pressure Vessel | Static |
| XV-401 | Control Valve | Valve |
| E-501 | Heat Exchanger | Static |

Enter a tag number such as `C-201` in E2.

## 3. Syntax

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

| Argument | Meaning |
|---|---|
| `lookup_value` | The value to search for |
| `table_array` | The range containing the lookup column and return data |
| `col_index_num` | The position of the return column within the selected range |
| `range_lookup` | FALSE for exact match; TRUE or omitted for approximate match |

For most equipment-register lookups, use FALSE to request an exact match.

## 4. First formula

In F2, enter:

```excel
=VLOOKUP(E2,$A$2:$C$6,2,FALSE)
```

Expected result: `Gas Compressor`.

Argument breakdown:
- `E2`: the tag number to find.
- `$A$2:$C$6`: the table range. Dollar signs lock the range when copying the formula.
- `2`: return the second column within the selected range (Equipment Description).
- `FALSE`: require an exact match.

**Important:** The column index is counted from the left edge of the selected table range, not from the worksheet's column letters.

For the range A2:C6:
- 1 = Tag Number
- 2 = Equipment Description
- 3 = Equipment Type

## 5. Guided exercises

Use the same table and change the lookup value in E2.

| Lookup value | Return column index | Expected result |
|---|---:|---|
| P-101 | 2 | Centrifugal Pump |
| V-301 | 3 | Static |
| XV-401 | 2 | Control Valve |
| E-501 | 3 | Static |

For example, to return Equipment Type:

```excel
=VLOOKUP(E2,$A$2:$C$6,3,FALSE)
```

## 6. Understand the left-to-right limitation

VLOOKUP searches only in the first column of the selected table range and returns values from columns to its right.

With the sample range A2:C6:
- Find a tag number and return its description: supported.
- Find a tag number and return its type: supported.
- Find an equipment description and return its tag number: not supported with this table arrangement.

XLOOKUP can handle lookup and return arrays in either order.

## 7. Practice checklist

- [ ] Enter the sample equipment register.
- [ ] Enter the formula manually.
- [ ] Complete all four guided exercises.
- [ ] Change the return column index from 2 to 3 and explain the difference.
- [ ] Change the lookup value to a tag that does not exist and observe the result.
- [ ] Explain why the dollar signs are used around the table range.
- [ ] Explain the left-to-right limitation.

## 8. Knowledge check

1. What does VLOOKUP stand for?
2. What does the first column of the table_array do?
3. In the formula above, why is the column index 2?
4. What is the difference between TRUE and FALSE in the range_lookup argument?
5. Why is the table range written as `$A$2:$C$6`?
6. Can VLOOKUP return a tag number when the lookup value is an equipment description in this table arrangement? Why?

**Completion rule:** Keep this lesson IN PROGRESS until the practice checklist and knowledge check are completed and reviewed.
