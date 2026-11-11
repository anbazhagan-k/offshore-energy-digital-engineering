# Excel Lesson 07 — IF and Nested IF

**Study date:** 2026-11-11  
**Status:** PRACTISED — additional exercise pending  
**Application:** Engineering equipment registers, inspection status, pressure classification and maintenance risk.

## Learning objectives

By the end of this lesson, the learner should be able to:

- Explain the purpose and syntax of the IF function.
- Build a logical test using comparison operators.
- Return different text results when a condition is TRUE or FALSE.
- Copy formulas down while allowing relative cell references to adjust.
- Recognise when numeric-looking values may be stored as text and use VALUE when appropriate.
- Build a Nested IF formula to classify data into more than two categories.
- Check boundary values carefully.

## 1. IF function

The IF function tests a condition and returns one value when the condition is TRUE and another when it is FALSE.

**Syntax**

```excel
=IF(logical_test, value_if_true, value_if_false)
```

Example: if the quantity is in B2, classify values greater than 5 as High.

```excel
=IF(B2>5,"High","Normal")
```

- `B2>5` is the logical test.
- `"High"` is returned when the test is TRUE.
- `"Normal"` is returned when the test is FALSE.

### Comparison operators

| Operator | Meaning |
|---|---|
| `=` | Equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `<>` | Not equal to |

### Practice example — inspection status

Rule: fewer than 0 inspection days remaining means Overdue; otherwise Within Schedule.

```excel
=IF(B2<0,"Overdue","Within Schedule")
```

A value of 0 is Within Schedule because 0 is not less than 0. This distinction reinforces the difference between `<0` and `<=0`.

### Practice example — quantity classification

Rule: quantity greater than or equal to 5 means Bulk; otherwise Limited.

```excel
=IF(B2>=5,"Bulk","Limited")
```

A quantity of exactly 5 is Bulk. The operator `>=` includes the boundary value.

### Practice example — maintenance priority

Rule: more than 180 days since maintenance means High Priority; otherwise Normal Priority.

```excel
=IF(B2>180,"High Priority","Normal Priority")
```

Exactly 180 days is Normal Priority because the rule says strictly greater than 180.

## 2. Numeric values stored as text

During practice, the formula `=IF(B2>5,"High","Normal")` returned High for every row, even where the visible quantity was 2, 3 or 5. The learner then used:

```excel
=IF(VALUE(B2)>5,"High","Normal")
```

This produced the expected classifications.

`VALUE(B2)` converts numeric text into a number that can be compared mathematically. If a formula behaves unexpectedly, check the underlying cell value and data type rather than assuming the logical test is wrong. Alignment can be a clue, but it is not conclusive proof of a cell's data type.

## 3. Nested IF

A Nested IF places another IF function inside the result argument of an earlier IF. It allows more than two possible classifications.

**Example — four pressure bands**

| Pressure (bar) | Classification |
|---:|---|
| Less than 15 | Low |
| 15 to less than 25 | Normal |
| 25 to less than 35 | High |
| 35 or above | Critical |

Formula, with pressure in B2:

```excel
=IF(B2<15,"Low",IF(B2<25,"Normal",IF(B2<35,"High","Critical")))
```

There are three IF functions, so there are three matching closing parentheses. Excel evaluates the tests from left to right and returns the result for the first TRUE condition.

### Five-band pressure example

| Pressure (bar) | Classification |
|---:|---|
| Less than 10 | Very Low |
| 10 to less than 20 | Low |
| 20 to less than 30 | Normal |
| 30 to less than 40 | High |
| 40 or above | Critical |

Formula:

```excel
=IF(B3<10,"Very Low",IF(B3<20,"Low",IF(B3<30,"Normal",IF(B3<40,"High","Critical"))))
```

The learner independently entered this formula and correctly classified all nine practice values: 8, 10, 18, 20, 29, 30, 39, 40 and 45.

## 4. Boundary-value reasoning

Always test values exactly at each threshold.

For the five-band example:

| Value | Expected classification | Reason |
|---:|---|---|
| 9 | Very Low | Less than 10 |
| 10 | Low | Not less than 10; less than 20 |
| 20 | Normal | Not less than 20; less than 30 |
| 30 | High | Not less than 30; less than 40 |
| 40 | Critical | Not less than 40 |

The order of conditions matters. With ascending thresholds, each later test is reached only after earlier tests have returned FALSE.

## 5. Practice completed in this session

The learner independently completed and reviewed:

1. Inspection status using `<0`, including negative, zero and positive values. One initial boundary mistake at zero was identified and corrected.
2. Quantity classification using `>=5`. The exact value 5 was initially misclassified using a strict greater-than test; the operator was corrected.
3. Maintenance priority using `>180`; all five results were correct.
4. Pressure classification using `>=20`; all five results were correct.
5. Four-band Nested IF pressure classification; all ten results were correct, including 15, 25 and 35.
6. Five-band Nested IF pressure classification; all nine results were correct, including 10, 20, 30 and 40.
7. Explained the concept of Nested IF and answered the conceptual check correctly (3/3).

## 6. Additional exercise — pending

Complete this maintenance-risk classification independently.

| Days since maintenance | Risk |
|---:|---|
| Less than 90 | Low |
| 90 to less than 180 | Moderate |
| 180 to less than 365 | High |
| 365 or above | Critical |

| Equipment tag | Days since maintenance |
|---|---:|
| P-101 | 45 |
| P-102 | 90 |
| C-201 | 150 |
| C-202 | 180 |
| V-301 | 250 |
| V-302 | 364 |
| E-401 | 365 |
| E-402 | 500 |
| XV-501 | 89 |

Write a Nested IF formula in the Risk column, fill it down, and verify the boundary values 90, 180 and 365.

## 7. Key takeaways

- IF evaluates one logical test and returns one of two outcomes.
- Comparison operators determine exactly how threshold values are treated.
- Relative references adjust when formulas are copied to other rows.
- VALUE can convert numeric text to a number for mathematical comparisons.
- Nested IF evaluates several conditions in sequence and stops at the first TRUE condition.
- Boundary values must be checked against the wording of the rule.

## Next lesson

Continue with logical functions: `AND`, `OR`, and combining them with `IF`. Do not mark the full logical-functions module complete until these topics and their exercises are covered.
