# Customers and Orders sample data

Use this small fictional dataset to check relationships, joins, and query inputs. It contains two customers and three orders.

## Customers

```csv
id,name
1,Ada
2,Grace
```

## Orders

```csv
id,customer_id,total
101,1,25
102,1,40
103,2,15
```

These identifiers describe the example. If Jet Tables generates its own primary keys during import, keep source identifiers in separate fields and use the corresponding field names when configuring the relationship. Do not assume imported source IDs become the Jet Tables primary keys.

## Expected results

| Check                      | Expected result                              |
| -------------------------- | -------------------------------------------- |
| Orders for customer 1      | Orders 101 and 102                           |
| Orders for customer 2      | Order 103                                    |
| Total for customer 1       | 65                                           |
| Orders joined to customers | Three rows; Ada appears twice and Grace once |
| Query for customer 3       | No rows                                      |

For matching tests, add an order with a missing customer identifier and inspect the result. Decide whether a join should keep unmatched orders or exclude them.

Use the dataset with [Relationships](relationships/), [Use dynamic SQL inputs](../sql-queries-and-api-requests/use-dynamic-sql-inputs.md), and [Join data from multiple sources](../synced-tables/join-data-from-multiple-sources.md).
