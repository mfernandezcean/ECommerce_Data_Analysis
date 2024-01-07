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

- Item Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  item_dim;

```

|  item_dim| num_rows |
|--|--|
| 1 |264|

- Store Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  store_dim;

```

|  store_dim| num_rows |
|--|--|
| 1 |726|

- Time Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  time_dim;

```

|  time_dim| num_rows |
|--|--|
| 1 |99,999|

- Transaction (*payment*) Table:
```
SELECT 
  COUNT(*) AS num_rows 
FROM 
  Trans_dim;

```

|  Trans_dim| num_rows |
|--|--|
| 1 |39|
