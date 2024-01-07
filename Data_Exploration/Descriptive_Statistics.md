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
