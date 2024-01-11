# Querying: 

- ## How sells more items?

## by Divisions

||division	  | Quantitysold |
|--|--|--|
|1| DHAKA	 | 2,319,920 |
|2|  CHITTAGONG	| 1,126,300 |
| 3| RAJSHAHI	|689,138  |
|4|KHULNA	  | 642,999 |
| 5| RANGPUR	|480,244  |
|6| BARISAL	 |428,042  |
| 7| SYLHET	|  313,542|

## INSIDE the Divisions: District's

#### Top 3 Districts by Division

### DHAKA:
```
SELECT 
  TOP 3(district), 
  sum(quantity) as Quantitysold 
FROM 
  fact_table 
  JOIN store_dim ON fact_table.store_key = store_dim.store_key 
WHERE 
  division = 'DHAKA' 
GROUP BY 
  district 
ORDER BY 
  Quantitysold DESC;
```

||district	| Quantitysold |
|--|--|--|
|1| DHAKA	 | 1,344,318|
|2|  KISHOREGONJ	| 108,202|
| 3| MYMENSINGH	|107,387|
