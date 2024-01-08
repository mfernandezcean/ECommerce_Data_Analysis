## Identify Outliers

- Fact Table:

### Quantity

```
SELECT 
  AVG(quantity) as mean, 
  STDEV(quantity) as std_dev, 
  min(quantity) as min_value, 
  Max(quantity) as max_value 
FROM 
  fact_table;

```

| mean	| std_dev	|min_value	| max_value
|--|--|--|--|
|6| 3.16193152417727	| 1|11

#### Z-Score:

```
WITH ZScoreCTE AS (
  SELECT 
    quantity, 
    (
      quantity - AVG(quantity) OVER ()
    ) / STDEV(quantity) OVER () AS ZScore 
  FROM 
    fact_table
) 
SELECT 
  * 
FROM 
  ZScoreCTE 
WHERE 
  ABS(ZScore) > 1;

```

![image](https://github.com/mfernandezcean/ECommerce_Data_Analysis/assets/105746149/3bed7f92-9588-4f56-b145-68ab746ae83c)

| Z-Score| Number of rows	|
|--|--|
|1| 363,606
|1.5|181,719
|2| 0

[Z-Score](https://umsystem.pressbooks.pub/isps/chapter/chapter-4/) is considered a solid method to identify outliers. When the threshold is either over or under 2.5, it is considered an outlier.

- in this Column of quantity, no outliers where found.

### Unit Price:

```
SELECT 
  AVG(unit_price) as mean, 
  STDEV(unit_price) as std_dev, 
  min(unit_price) as min_value, 
  Max(unit_price) as max_value 
FROM 
  fact_table;
```

| mean	| std_dev	|min_value	| max_value
|--|--|--|--|
|17.56160175	| 8.63709693047035		| 6|55



#### Z-Score:

```
WITH ZScoreCTE AS (
  SELECT 
    unit_price, 
    (
      unit_price - AVG(unit_price) OVER ()
    ) / STDEV(unit_price) OVER () AS ZScore 
  FROM 
    fact_table
) 
SELECT 
  * 
FROM 
  ZScoreCTE 
WHERE 
  ABS(ZScore) > 1 
ORDER BY 
  unit_price;

```

| Z-Score| Number of rows	|
|--|--|
|1| 204,907
|1.5|75,823
|2| 68,295
|2.5|57,105

[Z-Score](https://umsystem.pressbooks.pub/isps/chapter/chapter-4/) is considered a solid method to identify outliers. When the threshold is either over or under 2.5, it is considered an outlier.

- Outliers:

Z-score|unit_price|
|--|--|
|> 2.5|40|
|> 2.5|42|
|> 2.5|44|
|> 2.5|45|
|> 2.5|46|
|> 2.5|48|
|> 2.5|53|
|> 2.5|55|

## WHAT TO DO WITH THESE OUTLIERS???????????????????????????


### Total Price:

```
SELECT 
  AVG(total_price) as mean, 
  STDEV(total_price) as std_dev, 
  min(total_price) as min_value, 
  Max(total_price) as max_value 
FROM 
  fact_table;

```

| mean	| std_dev	|min_value	| max_value
|--|--|--|--|
|105.40143575	| 80.8293013000364	| 6|605

#### Z-Score:

```
WITH ZScoreCTE AS (
    SELECT
        total_price,
        (total_price - AVG(total_price) OVER ()) / STDEV(total_price) OVER () AS ZScore
    FROM fact_table
)
SELECT Distinct total_price
FROM ZScoreCTE
WHERE ABS(ZScore) > 2.5 
ORDER BY total_price;
```

| Z-Score| Number of rows	|
|--|--|
|1| 123
|1.5|68
|2| 51
|2.5|41
