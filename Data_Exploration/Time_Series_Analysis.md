## Time Series Analysis

### Year:

```
SELECT 
  year, 
  count(*) as num_records 
FROM 
  time_dim 
GROUP BY 
  year 
ORDER BY 
  year ASC;

```

|year	 |num_records |
|--|--|
|  2014	| 13,560 |
| 2015	 | 14,294 |
| 2016	 | 14,239 |
|  2017	| 14,357 |
|  2018	| 14,315 |
|  2019	|14,240  |
|  2020	| 14,160 |
|  2021	|  834|


### Quarter:

```
SELECT 
  quarter, 
  count(*) as num_records 
FROM 
  time_dim 
GROUP BY 
  quarter 
ORDER BY 
  quarter ASC;

```

| quarter	| num_records|
|--|--|
|1.00| 24,783
|2.00|24,838
|3.00| 2,5265
|4.00|25,113

### Month:

```
SELECT 
  month, 
  count(*) as num_records 
FROM 
  time_dim 
GROUP BY 
  month 
ORDER BY 
  month ASC;

```
|month|num_records |
|--|--|
|  1| 8,606|
| 2| 7,647|
| 3| 8,530|
|  4| 8,100|
|  5| 8,636 |
|  6|8,102|
|  7| 8,567|
|  8|  8,447|
|  9|  8,251|
|  10|  8,466|
|  11|  8,198|
|  12|  8,449|
