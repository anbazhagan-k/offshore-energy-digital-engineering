# Lesson 12 — MAXIFS and MINIFS

**Learning environment:** Google Sheets  
**Certification alignment:** Microsoft Office Specialist: Excel Expert (Microsoft 365 Apps), MO-211  
**Status:** COMPLETED — independent assessment passed 5/5 (2026-11-21)

## Learning objectives

- Find maximum and minimum values that meet one or more conditions.
- Apply multiple criteria using AND logic.
- Use numeric comparison criteria.
- Build dynamic criteria using cell references and concatenation.
- Apply date criteria and inclusive date ranges.
- Combine text, numeric and date conditions in one formula.

## Core practice

The learner practised MAXIFS and MINIFS syntax, single-condition criteria, multiple criteria, numeric thresholds, dynamic cell references and date ranges.

Examples:

```excel
=MAXIFS(C2:C20,B2:B20,"Instrumentation")
=MINIFS(C2:C20,B2:B20,"Mechanical",C2:C20,">15000")
=MAXIFS(C2:C20,B2:B20,"Electrical",D2:D20,">="&DATE(2026,1,1),D2:D20,"<="&DATE(2026,1,31))
```

Dynamic criteria must concatenate the operator with the cell reference:

```excel
">"&F2
```

Do not write `">F2"`, which is treated as literal text rather than a reference to F2.

## Independent assessment — 2026-11-21

The learner completed a five-question assessment:

1. Highest maintenance cost for Instrumentation equipment — correct.
2. Lowest Mechanical maintenance cost above ₹15,000 — correct.
3. Highest Electrical maintenance cost during January 2026 — correct.
4. Lowest Instrumentation maintenance cost above ₹20,000 during January 2026 — correct.
5. Highest Mechanical maintenance cost during January 2026, above the threshold in F2 — formula initially used `">F2"`; corrected to `">"&F2`.

**Result:** 5/5 completed correctly after feedback. The final dynamic-reference correction was understood and applied.

## Accuracy note

The assessment checked formula structure. No assessment dataset values were supplied, so actual returned results were not independently verified. Earlier date exercises were also checked for formula structure rather than calculated outputs.

## Completion status

**COMPLETED (2026-11-21).** Core practice and independent assessment are complete. Continue to the next planned formula topic after the current supplementary IFS advanced practice.
