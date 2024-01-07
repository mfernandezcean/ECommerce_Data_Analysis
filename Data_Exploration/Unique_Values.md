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
|  Customer Table| num_unique|
|--|--|
| coustomer_key |9,191|
| name| 4,534|
|contact_no | 9,190|
| nid|9,191 |

*Seems alright. Primary Key is unique and also nid (that is 'unique identification number for the customer'). Then the others is logical to have repetitions*
