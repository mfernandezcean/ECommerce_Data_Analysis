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

- Fact Table:
```
SELECT 
  Top(5) * 
FROM 
  fact_table;

```


| payment_key|customer_key|time_key|item_key|store_key |quantity | unit|unit_price|total_price
|--|--|--|--|--|--|--|--|--|
| 24.00|C005653|T045318| I00042| 206.00|9|bottles|28|252
| 11.00| C003919|T014917| I00122|85.00 |3|ct|15|45
|37.00| C005452 |T079513|I00035|587.00 |8|cans|16|128
|  16.00|  C007555|T026577|I00120|619.00 |8|ct|9|72
| 24.00|  C003316|T038477| I00244|178.00 |5|oz|18|90
  
