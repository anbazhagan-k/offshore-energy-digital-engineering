# Excel Lesson 08 — AND, OR and Combining Logical Functions

**Study date:** 2026-11-12  
**Status:** PRACTISED — core exercises verified  
**Application:** Equipment maintenance decisions, inspection prioritisation and engineering registers.

## Learning objectives

By the end of this lesson, the learner should be able to:

- Explain how AND and OR evaluate logical conditions.
- Use AND when every condition must be TRUE.
- Use OR when at least one condition must be TRUE.
- Combine IF with AND and OR.
- Interpret formula results and test boundary values.
- Build a multi-condition maintenance decision rule.

## 1. AND function

AND returns TRUE only when **all** supplied conditions are TRUE.

**Syntax**

```excel
=AND(logical1, [logical2], ...)
```

Example: return TRUE only when maintenance days in B2 are at least 180 and priority in C2 is Critical.

```excel
=AND(B2>=180,C2="Critical")
```

If either condition is FALSE, AND returns FALSE.

## 2. OR function

OR returns TRUE when **at least one** supplied condition is TRUE.

**Syntax**

```excel
=OR(logical1, [logical2], ...)
```

Example: return TRUE when maintenance days in B2 are at least 365 or priority in C2 is Critical.

```excel
=OR(B2>=365,C2="Critical")
```

OR returns FALSE only when all its conditions are FALSE.

## 3. IF with AND

Business rule: mark equipment for immediate attention only when maintenance days are at least 180 **and** priority is High.

```excel
=IF(AND(B2>=180,C2="High"),"Yes","No")
```

The AND function evaluates both conditions. IF then converts the TRUE/FALSE result into the requested text.

## 4. IF with OR

Business rule: inspection is required if maintenance days are at least 365 **or** priority is Critical.

```excel
=IF(OR(B2>=365,C2="Critical"),"Yes","No")
```

The learner independently supplied the formula and correctly classified all seven cases:

| Equipment | Days | Priority | Expected result |
|---|---:|---|---|
| P-101 | 400 | Low | Yes |
| P-102 | 200 | Critical | Yes |
| C-201 | 100 | High | No |
| C-202 | 365 | High | Yes |
| V-301 | 150 | Critical | Yes |
| V-302 | 250 | Low | No |
| E-401 | 364 | High | No |

**Verified result: 7/7 correct.**

Boundary lesson: 365 qualifies for `>=365`; 364 does not. A Critical priority independently satisfies the OR condition.

## 5. Combining IF, AND and OR

Business rule: equipment requires Immediate Attention if either:

- Condition A: maintenance days are at least 365; **OR**
- Condition B: maintenance days are at least 180 **AND** priority is Critical.

In plain language:
- 365 days or more → Immediate Attention, regardless of priority.
- At least 180 days and Critical priority → Immediate Attention.
- Otherwise → Normal.

**Formula**

```excel
=IF(OR(B2>=365,AND(B2>=180,C2="Critical")),"Immediate Attention","Normal")
```

Read the formula from the inside out:

1. `AND(B2>=180,C2="Critical")` checks whether both parts of Condition B are TRUE.
2. `OR(B2>=365,AND(...))` checks whether Condition A or Condition B is TRUE.
3. `IF(...,"Immediate Attention","Normal")` returns the business outcome.

### Verified practice results

| Equipment | Days | Priority | Expected result |
|---|---:|---|---|
| P-101 | 400 | Low | Immediate Attention |
| P-102 | 200 | Critical | Immediate Attention |
| C-201 | 100 | High | Normal |
| C-202 | 365 | High | Immediate Attention |
| V-301 | 150 | Critical | Normal |
| V-302 | 250 | Low | Normal |
| E-401 | 180 | Critical | Immediate Attention |
| E-402 | 179 | Critical | Normal |
| XV-501 | 364 | High | Normal |

**Verified result: 9/9 correct.**

Important boundary cases:
- 400 days + Low → Immediate Attention because Condition A is TRUE.
- 200 days + Critical → Immediate Attention because both parts of Condition B are TRUE.
- 150 days + Critical → Normal because the 180-day threshold in Condition B is not met.
- 179 days + Critical → Normal for the same reason.
- 365 days qualifies; 364 does not.

## 6. Key takeaways

| Function / combination | Logic |
|---|---|
| `AND(condition1, condition2)` | Every condition must be TRUE |
| `OR(condition1, condition2)` | At least one condition must be TRUE |
| `IF(AND(...),...,...)` | Make a decision when all conditions are met |
| `IF(OR(...),...,...)` | Make a decision when at least one condition is met |
| `IF(OR(A,AND(B,C)),...,...)` | A OR (B AND C) |

Parentheses control which conditions are evaluated together. Translate the business rule into plain language before writing the formula.

## 7. Practice evidence and status

- IF + OR formula: learner supplied the correct formula; 7/7 results verified.
- IF + AND: learner correctly applied the combined condition in a six-record practice; all six predicted outcomes were correct.
- IF + OR + AND: learner correctly classified all nine equipment records; 9/9 verified.
- The learner has practised the core logic. Additional independent revision can be used later to reinforce it.

## Next lesson

Study COUNTIF and COUNTIFS to count records that meet one or multiple conditions. Continue with text criteria, numerical comparisons and practical equipment-register reporting.
