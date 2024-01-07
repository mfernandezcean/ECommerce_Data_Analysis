## Explore for Unique Values:
- Customer Table:
```
SELECT 
  COUNT(DISTINCT coustomer_key) AS num_unique 
FROM 
  customer_dim;

SELECT 
  COUNT(DISTINCT name) AS num_unique 
FROM 
  customer_dim;

SELECT 
  COUNT(DISTINCT contact_no) AS num_unique 
FROM 
  customer_dim;

SELECT 
  COUNT(DISTINCT nid) AS num_unique 
FROM 
  customer_dim;

```
|  Customer Table| num_unique|total_rows
|--|--|--|
| coustomer_key |9,191|9,191
| name| 4,534|9,191
|contact_no | 9,190|9,191
| nid|9,191 |9,191

*Seems alright. Primary Key is unique and also nid (that is 'unique identification number for the customer'). Then the others is logical to have repetitions*

- Fact Table:

```
SELECT 
  COUNT(DISTINCT payment_key) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT coustomer_key) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT time_key) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT item_key) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT store_key) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT quantity) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT unit) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT unit_price) as num_unique 
FROM 
  fact_table;

SELECT 
  COUNT(DISTINCT total_price) as num_unique 
FROM 
  fact_table;

```

|  Fact Table| num_unique| total_rows
|--|--|--|
| payment_key|39|1,000,000
| coustomer_key| 9,191|1,000,000
|time_key| 99,993|1,000,000
| item_key|264|1,000,000
| store_key| 726|1,000,000
|quantity | 11|1,000,000
| unit|16 |1,000,000
| unit_price| 46|1,000,000
| total_price|285 |1,000,000

*This is a fact table so repetition is expected. Checking with the primary key's in the dimension tables is more relevant*

- Item Table:

```
SELECT 
  COUNT(DISTINCT item_key) AS num_unique 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT item_name) AS num_unique 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT[desc]) 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT unit_price) AS num_unique 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT man_country) AS num_unique 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT supplier) AS num_unique 
FROM 
  item_dim;

SELECT 
  COUNT(DISTINCT unit) AS num_unique 
FROM 
  item_dim;

```

|  Item Table| num_unique| total_rows
|--|--|--|
| item_key|294|294
| item_name|259|294
|desc| 29|294
| unit_price|46|294
| man_country| 10|294
|supplier | 10|294
| unit|16 |294

- Store Table:

```
SELECT 
  COUNT(DISTINCT store_key) AS num_unique 
FROM 
  store_dim;

SELECT 
  COUNT(DISTINCT division) AS num_unique 
FROM 
  store_dim;

SELECT 
  COUNT(DISTINCT district) AS num_unique 
FROM 
  store_dim;

SELECT 
  COUNT(DISTINCT upazila) AS num_unique 
FROM 
  store_dim;

```

|  Store Table| num_unique| total_rows
|--|--|--|
| store_key|726|726
| division|7|726
|district| 64|726
| upazila|540|726
  
