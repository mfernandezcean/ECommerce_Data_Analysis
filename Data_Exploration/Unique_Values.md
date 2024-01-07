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

|  FactTable| num_unique| total_rows
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

*this is a fact table so repetition is expected. Checking with the primary key's in the dimension tables is more relevant*
