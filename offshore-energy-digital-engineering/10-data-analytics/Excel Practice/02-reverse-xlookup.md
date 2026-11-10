# Lesson 02 — Reverse XLOOKUP: Return a Value from the Left

<escape>**Objective:**</escape> Use XLOOKUP when the return column is to the left of the lookup column.

## 1. Understand the problem

In a traditional VLOOKUP, the lookup column must be the first column in the selected table range, and the return column must be to its right. XLOOKUP does not have this limitation.

For example, suppose an equipment register has the description in column A and the tag number in column B. You know the tag number and need to return the description. The return column (A) is to the left of the lookup column (B).

## 2. Sample equipment register

Enter this data in cells A1:D6:

| Equipment Description | Tag Number | Equipment Type | Location |
|---|---|---|---|
| Centrifugal Pump | P-101 | Rotating | Process Area A |
| Gas Compressor | C-201 | Rotating | Compression Area |
| Pressure Vessel | V-301 | Static | Process Area B |
| Control Valve | XV-401 | Valve | Pipe Rack 1 |
| Heat Exchanger | E-501 | Static | Utility Area |

Enter a tag number in F2, for example `C-201`.

## 3. Formula

In G2, enter:

```excel
=XLOOKUP(F2,B2:B6,A2:A6,"Tag not found")
```

### Understand each argument

| Argument | Meaning | In this example |
|---|---|---|
| `F2` | lookup_value | The tag number to find |
| `B2:B6` | lookup_array | The column containing tag numbers |
| `A2:A6` | return_array | The column containing descriptions |
| `"Tag not found"` | if_not_found | Message when no match exists |

**Expected result:** `Gas Compressor`

Notice that the lookup array is B2:B6 and the return array is A2:A6. The return array is to the left, and the formula still works.

## 4. Guided exercises

Keep the same data. Change the value in F2 and use the formula in G2.

| Exercise | F2 input | Expected result |
|---:|---|---|
| 1 | C-201 | Gas Compressor |
| 2 | V-301 | Pressure Vessel |
| 3 | XV-401 | Control Valve |
| 4 | P-999 | Tag not found |

## 5. Return a different column

To return the equipment type for the tag number in F2:

```excel
=XLOOKUP(F2,B2:B6,C2:C6,"Tag not found")
```

To return the location:

```excel
=XLOOKUP(F2,B2:B6,D2:D6,"Tag not found")
```

## 6. Key distinction: left lookup vs reverse search

These are two different ideas:

- **Lookup to the left:** the return column is positioned to the left of the lookup column. This is handled by selecting the appropriate lookup and return arrays.
- **Search from bottom to top:** find the last matching item when duplicates exist. This uses the XLOOKUP `search_mode` argument, typically `-1`, and will be covered in Lesson 03.

## 7. Your practice checklist

- [ ] Build the sample table in Excel.
- [ ] Enter the formula yourself rather than copying it.
- [ ] Complete all four guided exercises.
- [ ] Change the return array from A2:A6 to C2:C6 and D2:D6.
- [ ] Explain why this is called a lookup to the left.
- [ ] Explain how this differs from searching from bottom to top.

## 8. Knowledge check

1. Which argument contains the tag numbers?
2. Which argument contains the equipment descriptions?
3. Why does this formula work even though the description column is to the left?
4. What message should appear when the lookup value is P-999?
5. Is a left lookup the same as a bottom-to-top search? Explain.

**Completion status:** IN PROGRESS — mark this lesson complete only after the practice and knowledge check are finished.
