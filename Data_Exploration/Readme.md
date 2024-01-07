## Data Exploration:

### Count number of rows of tables:
- Customer Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  customer_dim;

```
|  customer_dim| num_rows |
|--|--|
| 1 |9,191  |

- Fact Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  fact_table;

```

|  fact_table| num_rows |
|--|--|
| 1 |1,000,000|
