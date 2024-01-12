# Querying: 

- ## Where more items are sold?

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

### CHITTAGONG:

||district	| Quantitysold |
|--|--|--|
|1| CHITTAGONG	| 415,284|
|2|  COMILLA	| 131,255|
| 3| RANGAMATI	|83,069|

### RAJSHAHI:

||district	| Quantitysold |
|--|--|--|
|1| RAJSHAHI	| 214,163|
|2|  BOGRA	| 98,039|
| 3| NAOGAON	|89,116|

### KHULNA:

||district	| Quantitysold |
|--|--|--|
|1| KHULNA	| 231,976|
|2|  BAGERHAT	| 74,549|
| 3| JESSORE	|64,459|

### RANGPUR:

||district	| Quantitysold |
|--|--|--|
|1| DINAJPUR	| 106,492|
|2|  KURIGRAM	| 75,200|
| 3| RANGPUR	|67,435|


### BARISAL:

||district	| Quantitysold |
|--|--|--|
|1| BARISAL	| 163,782|
|2|  PATUAKHALI	| 66,096|
| 3| BHOLA	|58,248|


### SYLHET:

||district	| Quantitysold |
|--|--|--|
|1| SYLHET	| 98,609|
|2|  SUNAMGANJ	| 90,457|
| 3| HABIGANJ	|65,937|

- ## How buys more items?

```
SELECT 
  TOP 10 name, 
  division, 
  sum(quantity) as Quantitysold 
FROM 
  fact_table 
  JOIN customer_dim ON fact_table.coustomer_key = customer_dim.coustomer_key 
  JOIN store_dim ON fact_table.store_key = store_dim.store_key 
GROUP BY 
  name, 
  division 
ORDER BY 
  Quantitysold DESC;

```


||name	| division	|Quantitysold |
|--|--|--|--|
|1| pooja	| DHAKA	| 46,823 |
|2|  jyoti	| DHAKA	|29,130|
| 3| pooja	|CHITTAGONG	|22,828|
| 4| neha	|DHAKA	| 22,170 |
| 5| sunita	|DHAKA	| 20,385 |
| 6| poonam	|DHAKA	|20,132  |
| 7| priyanka	|priyanka	| 18,123 |
| 8| seema	|DHAKA	|17,458  |
| 9| suman	|DHAKA	|16,591  |
| 10| mamta	|DHAKA	| 15,190 |


- ## When the items where sold?

```
SELECT 
  Year, 
  -- name, 
  --division,
  sum(quantity) as Quantitysold, 
  sum(total_price) as Income 
FROM 
  fact_table 
  JOIN customer_dim ON fact_table.coustomer_key = customer_dim.coustomer_key 
  JOIN store_dim ON fact_table.store_key = store_dim.store_key 
  JOIN time_dim ON fact_table.time_key = time_dim.time_key 
GROUP BY 
  Year 
ORDER BY 
  Year ASC;


```

| Year	 | Quantitysold	 | Income|
|--|--|--|
| 2014	 | 816,121	 | 14,334,731|
|2015	  |  859,999	| 15,095,720|
| 2016	 | 851,852	 |14,976,508 |
| 2017	 |854,563	  | 15,015,806|
| 2018	 |859,258	  | 15,108,197|
|  2019	|  851,282	| 14,949,510|
| 2020	 | 857,005	 | 15,037,190|
|2021 *(only 1 month)*	| 50,105	 |883,772 |
