# Basic info:

## Count number of rows of tables:
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
---
## Examine First Rows:
- Customer Table:
```
SELECT 
  Top(5) * 
FROM 
  customer_dim;

```
| customer_key |name  |contact_no |nid |
|--|--|--|--|
| C000001 |sumit  |8801920345851 | 7505075708899|
| C000002 | tammanne |8801817069329 | 1977731324842|
|C000003  | kailash kumar |8801663795774 |3769494056318 |
|  C000004|  bhagwati prasad|8801533627961 |9378834712725 |
| C000005 |  ajay|8801943715786 | 3540815556323|
  
