# Excel Fundamentals 03 — Relative, Absolute and Mixed References

**Training date:** 2026-11-10  
**Status:** PRACTISED — learner reports confidence

## Concepts covered

A cell reference tells Excel where to retrieve a value.

| Reference | Behaviour |
|---|---|
| `A1` | Relative: row and column can change when copied |
| `$A$1` | Absolute: row and column stay fixed |
| `$A1` | Mixed: column A stays fixed; row can change |
| `A$1` | Mixed: row 1 stays fixed; column can change |

## Practical examples

Relative formula:
```excel
=B2*C2
```
Copied one row down, it becomes `=B3*C3`.

Absolute-reference example, with the tax rate stored in F1:
```excel
=B2*$F$1
```
Copied one row down, it becomes `=B3*$F$1`.

The F4 key cycles through reference styles in many desktop versions of Excel. Laptop keyboards may require Fn+F4.

## Learning evidence

The learner reported completing exercises and feeling confident with relative, absolute and mixed references.

## Next action

Revisit mixed references in a two-dimensional copy-across-and-down exercise if uncertainty arises.
