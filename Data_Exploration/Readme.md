## Data Exploration:
- [Number](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Basic_information.md) of Rows of each table:
  
|  Table Name| num_rows |
|--|--|
| Customer Table |9,191|
| Fact Table| 1,000,000|
|Item Table | 264|
| Store Table|726 |
| Time Table|99,999 |
| Transaction (_payment_) Table| 39|

- Missing Values:

[27](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Missing_Values.md) names are missing from the customer table.

- Descriptive Statistcs:

#### [Fact Table](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Descriptive_Statistics.md):

| Item| Mean|Min| Max|Median
|--|--|--|--|--|
|Quantity| 6| 1|11 | 6
|Unit Price| 17.56160175| 6|55| 16
|Total Price| 105.40143575| 6|605| 90

#### [Item Table](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Descriptive_Statistics.md):

| Item| Mean|Min| Max|Median
|--|--|--|--|--|
|Unit Price| 17.5549242424242| 6|55| 16




- #### [Outliers](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Identify_Outliers.md)

In general, the outliers of these tables seem to have logic. So no further actions were made.

### Fact Table:

Unit Price :

 - 40
 - 42
 - 44
 - 45
 - 46
 - 48
 - 53
 - 55

Total Price :

 - 308
 - 315
 - 318
 - 319
 - ...
 - 530
 - 550
 - 583
 - 605

### Item Table:

Total Price :

 - 40
 - 42
 - 44
 - 45
 - 46
 - 48
 - 53
 - 55

- [Time Analysis](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Exploration/Time_Series_Analysis.md)

Distribution of the item's analyzed seem to have no seasonality or any other aspect that stand's out. Example:

Quarter : 


| quarter	| num_records|
|--|--|
|1.00| 24,783
|2.00|24,838
|3.00| 25,265
|4.00|25,113
