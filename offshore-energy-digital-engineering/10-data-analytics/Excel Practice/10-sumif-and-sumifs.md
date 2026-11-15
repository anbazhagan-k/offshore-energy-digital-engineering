# Lesson 10 — SUMIF and SUMIFS

**Status:** COMPLETED — independent assessment 5/5  
**Completed:** 2026-11-15  
**Learning context:** Excel practice for engineering information and offshore asset data management.

## Learning objectives

- Use SUMIF to sum values that meet one condition.
- Use SUMIFS to sum values that meet multiple conditions.
- Apply text, numerical, range and wildcard criteria.
- Use cell references to make criteria dynamic.
- Combine AND and OR logic in practical cost-analysis formulas.
- Distinguish hardcoded criteria from cell-reference criteria.

## 1. SUMIF — one condition

Syntax:

`=SUMIF(range, criteria, [sum_range])`

- `range`: cells Excel checks against the condition.
- `criteria`: the condition to match.
- `sum_range`: cells to add when the condition matches.

Example: sum maintenance cost for Pumps:

`=SUMIF(B2:B9,"Pump",C2:C9)`

The learner correctly calculated ₹27,000.

### Numerical criteria

Examples practised:

- `=SUMIF(C2:C9,">15000",C2:C9)`
- `=SUMIF(C2:C9,"<=15000",C2:C9)`

The learner correctly distinguished strict and inclusive comparisons: `>15000` excludes 15,000, while `>=15000` includes it.

### Cell-reference criteria

Example:

`=SUMIF(B2:B9,E2,C2:C9)`

When E2 contains `Pump`, the result is ₹27,000. Changing E2 to `Valve` changes the result to ₹12,000.

### Wildcard criteria

The learner practised:

- `"Pump*"` — starts with Pump.
- `"*Pump"` — ends with Pump.
- `"*Pump*"` — contains Pump anywhere.
- `"P?mp"` — one character in place of `?`.

Example:

`=SUMIF(A2:A6,"Pump*",B2:B6)`

The matching Pump records total ₹45,000. The learner independently used `"*Pump*"` and obtained the same total for the supplied dataset.

## 2. SUMIFS — multiple conditions

Syntax:

`=SUMIFS(sum_range, criteria_range1, criteria1, [criteria_range2, criteria2], ...)`

Important distinction:
- SUMIF starts with the criteria range.
- SUMIFS starts with the sum range.

SUMIFS applies AND logic: every supplied condition must be satisfied.

Example — Pump AND Critical:

`=SUMIFS(D2:D9,B2:B9,"Pump",C2:C9,"Critical")`

Result: ₹30,000.

The learner also correctly practised:
- Three conditions, including a numerical threshold.
- Criteria supplied through cell references.
- Numerical criteria greater than a threshold.
- A lower and upper numerical bound using the same sum column as a criteria range.

### Dynamic numerical criteria

With F2 = Critical, G2 = 10000 and H2 = 20000:

`=SUMIFS(D2:D9,C2:C9,F2,D2:D9,">"&G2,D2:D9,"<"&H2)`

Result: ₹30,000.

The learner correctly used concatenation (`&`) to combine a comparison operator with a cell reference.

## 3. Hardcoded criteria versus dynamic references

Hardcoded example:

`=SUMIFS(D2:D9,C2:C9,"Critical",D2:D9,">10000",D2:D9,"<20000")`

Dynamic example:

`=SUMIFS(D2:D9,C2:C9,F2,D2:D9,">"&G2,D2:D9,"<"&H2)`

Hardcoding means typing the value or condition directly into a formula. Cell references allow the user to change criteria in worksheet cells without editing the formula. Dynamic references are particularly useful in reusable reports and dashboards.

## 4. OR logic with SUMIFS

SUMIFS applies AND logic within one calculation. To calculate a total for either of two mutually exclusive text categories, add two SUMIFS calculations.

Example — Critical OR High:

`=SUMIFS(D2:D9,C2:C9,"Critical")+SUMIFS(D2:D9,C2:C9,"High")`

Result: ₹1,27,000.

The learner independently used cell references for the two criteria:

`=SUMIFS(D2:D9,C2:C9,F2)+SUMIFS(D2:D9,C2:C9,G2)`

## 5. Combined AND + OR logic

Each group uses AND conditions; the groups are joined using addition (OR).

Example:

- Group A: Pump AND Critical.
- Group B: Compressor AND High.

`=SUMIFS(D2:D9,B2:B9,"Pump",C2:C9,"Critical")+SUMIFS(D2:D9,B2:B9,"Compressor",C2:C9,"High")`

Result: ₹60,000.

### Important double-counting note

If one record satisfies both SUMIFS groups, adding the two results counts that record's value twice. The learner encountered this in a practice challenge where Compressor C-101 qualified for both groups. The requested sum of group totals was ₹80,000, with C-101 counted in both groups. If the business requirement is to total each qualifying record only once, the formula must account for the overlap.

## 6. Data type troubleshooting

During the independent assessment, a SUMIF formula returned 0.00 because the maintenance-cost values were stored as text. The learner converted the values into numeric values in a helper column (Column D), then confirmed the result was ₹77,000.

A conversion formula used during troubleshooting was:

`=VALUE(SUBSTITUTE(SUBSTITUTE(C2,"₹",""),",",""))`

After conversion, the numerical maintenance-cost values in D2:D9 were used for subsequent assessment questions.

## Independent assessment — passed 5/5

The final assessment used this worksheet layout:

- Column A: Equipment type
- Column B: Priority
- Column C: original maintenance-cost text
- Column D: converted numerical maintenance cost

1. Maintenance cost > ₹20,000: `=SUMIF(D2:D9,">20000",D2:D9)` → ₹77,000. Passed after identifying and correcting the text-versus-number issue.
2. Pump AND Critical: `=SUMIFS(D2:D9,B2:B9,"Critical",A2:A9,"Pump")` → ₹30,000. Correct formula and result.
3. Critical AND maintenance cost > ₹15,000: `=SUMIFS(D2:D9,B2:B9,"Critical",D2:D9,">15000")` → ₹43,000. Correct.
4. Critical OR High: `=SUMIFS(D2:D9,B2:B9,"Critical")+SUMIFS(D2:D9,B2:B9,"High")` → ₹1,27,000. The learner first supplied an AND-style formula; after explanation, corrected it to two SUMIFS calculations added together.
5. (Pump AND Critical) OR (Compressor AND High): `=SUMIFS(D2:D9,B2:B9,"Critical",A2:A9,"Pump")+SUMIFS(D2:D9,A2:A9,"Compressor",B2:B9,"High")` → ₹60,000. Correct.

**Assessment score: 5/5 passed.** Question 4 was passed after a correction and explanation; the learner independently supplied the correct formula for Question 5.

## Completion status

**Lesson 10 — SUMIF and SUMIFS: COMPLETED.**

The learner completed concept explanations, independent practice, formula verification, troubleshooting and a five-question assessment.

## Next lesson

AVERAGEIF and AVERAGEIFS, using offshore equipment performance and maintenance datasets.
