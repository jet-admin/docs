---
description: Choose formulas, lookups, rollups, or JavaScript to derive field values.
---

# Computed fields

Computed fields derive values from existing data. Choose the method that matches the calculation.

| Task                                         | Guide                              |
| -------------------------------------------- | ---------------------------------- |
| Calculate, combine text, or apply conditions | [Formulas](formulas/)              |
| Display a value from a linked record         | [Lookup](lookup-column.md)         |
| Aggregate values from related records        | [Rollup](rollup-column.md)         |
| Write a custom calculation                   | [JavaScript](javascript-column.md) |

Create the [relationship](../relationships/) before configuring a lookup or rollup.

## Add and verify a calculation

1. Choose the required fields and decide what result you expect for a sample record.
2. Add the computed field and configure its formula or related values.
3. Compare the result with a manual calculation.
4. Check a record with missing values and one with no related records.

Computed values are derived outputs. Edit their inputs to change the result. Availability of filtering and sorting depends on the field type and context.
