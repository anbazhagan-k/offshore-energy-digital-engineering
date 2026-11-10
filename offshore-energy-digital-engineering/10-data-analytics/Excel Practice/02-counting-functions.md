# Excel Fundamentals 02 — MIN, COUNT, COUNTA and COUNTBLANK

**Training date:** 2026-11-10  
**Status:** STUDIED — independent assessment not recorded

## Concepts covered

| Function | Purpose |
|---|---|
| MIN | Returns the smallest numeric value |
| COUNT | Counts cells containing numbers |
| COUNTA | Counts non-empty cells, including text and numbers |
| COUNTBLANK | Counts empty cells |

Examples:
```excel
=MIN(C2:C7)
=COUNT(C2:C7)
=COUNTA(B2:B7)
=COUNTBLANK(B2:B7)
```

## Engineering register application

These functions can help check quantities and completeness of equipment registers. For example, COUNTBLANK can identify missing equipment descriptions or quantities.

## Practice dataset

| Tag Number | Equipment | Quantity |
|---|---|---:|
| P-101 | Pump | 5 |
| C-201 | Compressor | 3 |
| V-301 | *(blank)* | 2 |
| E-401 | Heat Exchanger | 4 |
| XV-501 | *(blank)* | 6 |
| P-601 | Pump | *(blank)* |

Expected checks:
- MIN quantity = 2
- COUNT quantities = 5
- COUNTA equipment descriptions = 4
- COUNTBLANK descriptions = 2
- COUNTBLANK quantities = 1

## Next action

Complete the independent knowledge check and repeat the formulas in Excel before marking this lesson complete.
