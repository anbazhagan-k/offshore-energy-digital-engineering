# Excel Fundamentals 04 — Copying Formulas and Fill Handle

**Training date:** 2026-11-10  
**Status:** STUDIED AND PRACTISED

## Concepts covered

The Fill Handle is the small square at the bottom-right corner of a selected cell. Dragging it copies formulas or extends patterns.

Example in D2:
```excel
=B2*C2
```

When filled down, relative references adjust:
- D2: `=B2*C2`
- D3: `=B3*C3`
- D4: `=B4*C4`

An absolute reference such as `$F$1` remains fixed when the formula is copied.

Other methods:
- Ctrl+C / Ctrl+V copies and pastes.
- Double-clicking the Fill Handle can fill a formula down alongside adjacent data, where Excel can determine the range.

## Practice task

Calculate total cost for multiple equipment rows, then calculate GST using a fixed tax-rate cell and copy the GST formula down.

## Learning evidence

The learner confirmed doing exercises and proceeded to the next chapter. A formal score was not recorded.
