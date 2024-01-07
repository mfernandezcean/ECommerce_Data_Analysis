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
  
- Item Table:
```
SELECT 
  Top(5) * 
FROM 
  item_dim;

```


| item_key|item_name|desc|unit_price|man_country |supplier | unit|
|--|--|--|--|--|--|--|
| I00001|A&W Root Beer - 12 oz cans|a. Beverage - Soda| 11.5| Netherlands|Bolsius Boxmeer|cans
| I00002| A&W Root Beer Diet - 12 oz cans|a. Beverage - Soda| 6.75|poland |CHROMADURLIN S.A.S|cans
|I00003| Barq's Root Beer - 12 oz cans |a. Beverage - Soda|6.75|Bangladesh |DENIMACH LTD|cans
|  I00004|  Cherry Coke 12oz|a. Beverage - Soda|6.75|Netherlands |Bolsius Boxmeer|cans
| I00005|  Cherry Coke Zero 12 pack|a. Beverage - Soda| 6.75|Finland |HARDFORD AB|cans

- Store Table:
```
SELECT 
  Top(5) * 
FROM 
  store_dim;

```
| store_key |division  |district |upazila |
|--|--|--|--|
| 1.00 |SYLHET  |HABIGANJ | AJMIRIGANJ|
| 2.00 | SYLHET |HABIGANJ | BAHUBAL|
|3.00  | SYLHET |HABIGANJ |BANIACHONG |
|  4.00|  SYLHET|HABIGANJ |CHUNARUGHAT |
| 5.00 |  SYLHET|HABIGANJ | HABIGANJ SADAR|

- Time Table:
```
SELECT 
  Top(5) * 
FROM 
  time_dim;

```


| time_key|date|hour|day|week |month | quarter|year
|--|--|--|--|--|--|--|--|
| T00001|2017-05-20 14:56:00.0000000|14| 20| 3rd Week|5|2.00|2017
|T00002| 2015-01-30 22:14:00.0000000|22| 30|4th Week |1|1.00|2015
|T00003| 2020-03-14 02:34:00.0000000 |2|14|2nd Week |3|1.00|2020
|  T00004|  2018-04-27 12:19:00.0000000|12|27|4th Week|4|2.00|2018
| T00005|  2018-04-14 10:43:00.0000000|10| 14|2nd Week |4|2.00|2018
  
