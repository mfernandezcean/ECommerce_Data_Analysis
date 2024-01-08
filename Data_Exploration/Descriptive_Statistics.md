## Descriptive Statistics:

- Fact Table:

### Quantity:

```
SELECT 
  AVG(quantity) AS Quantity_mean, 
  MIN(quantity) AS Quantity_min_value, 
  MAX(quantity) AS Quantity_max_value, 
  (
    (
      SELECT 
        MAX(quantity) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT quantity 
          FROM 
            fact_table 
          ORDER BY 
            quantity
        ) AS BottomHalf
    ) + (
      SELECT 
        MIN(quantity) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT quantity 
          FROM 
            fact_table 
          ORDER BY 
            quantity DESC
        ) AS TopHalf
    )
  ) / 2 AS Quantity_median 
FROM 
  fact_table;
```
| Quantity_mean	|Quantity_min_value	 | Quantity_max_value	|Quantity_median
|--|--|--|--|
|6 | 1| 11	|6


### Unit Price:

```
SELECT 
  AVG(unit_price) AS Unit_Price_mean, 
  MIN(unit_price) AS Unit_Price_min_value, 
  MAX(unit_price) AS Unit_Price_max_value, 
  (
    (
      SELECT 
        MAX(unit_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT unit_price 
          FROM 
            fact_table 
          ORDER BY 
            unit_price
        ) AS BottomHalf
    ) + (
      SELECT 
        MIN(unit_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT unit_price 
          FROM 
            fact_table 
          ORDER BY 
            unit_price DESC
        ) AS TopHalf
    )
  ) / 2 AS Unit_Price_median 
FROM 
  fact_table;

```


| Unit_Price_mean	|Unit_Price_min_value	| Unit_Price_max_value	|Unit_Price_median
|--|--|--|--|
|17.56160175	| 6| 55	|16

### Total Price:

```
SELECT 
  AVG(total_price) AS Total_Price_mean, 
  MIN(total_price) AS Total_Price_min_value, 
  MAX(total_price) AS Total_Price_max_value, 
  (
    (
      SELECT 
        MAX(total_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT total_price 
          FROM 
            fact_table 
          ORDER BY 
            total_price
        ) AS BottomHalf
    ) + (
      SELECT 
        MIN(total_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT total_price 
          FROM 
            fact_table 
          ORDER BY 
            total_price DESC
        ) AS TopHalf
    )
  ) / 2 AS Total_Price_median 
FROM 
  fact_table;

```

| Total_Price_mean	|Total_Price_min_value	| Total_Price_max_value	|Total_Price_median
|--|--|--|--|
|105.40143575	| 6| 605	|90

- Item Table:

### Unit Price:

```
SELECT 
  AVG(unit_price) AS Unit_Price_mean, 
  MIN(unit_price) AS Unit_Price_min_value, 
  MAX(unit_price) AS Unit_Price_max_value, 
  (
    (
      SELECT 
        MAX(unit_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT unit_price 
          FROM 
            item_dim 
          ORDER BY 
            unit_price
        ) AS BottomHalf
    ) + (
      SELECT 
        MIN(unit_price) 
      FROM 
        (
          SELECT 
            TOP 50 PERCENT unit_price 
          FROM 
            item_dim 
          ORDER BY 
            unit_price DESC
        ) AS TopHalf
    )
  ) / 2 AS Unit_Price_median 
FROM 
  item_dim;

```

| Unit_Price_mean	|Unit_Price_min_value	| Unit_Price_max_value	|Unit_Price_median
|--|--|--|--|
|17.5549242424242	| 6| 55	|16
