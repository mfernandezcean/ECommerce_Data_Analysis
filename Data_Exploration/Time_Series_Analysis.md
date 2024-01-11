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
