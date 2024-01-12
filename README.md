# ECommerce_Data_Analysis

![dataset-cover](https://github.com/mfernandezcean/ECommerce_Data_Analysis/assets/105746149/05cbb1a5-1bb4-4ec2-b5ed-2f7ec411f61f)

## Situation:
These data sets contain information about E-commerce transactions that occurred in various countries, suppliers, and items, etc. This Data is been created by [MIT license](https://www.mit.edu/~amini/LICENSE.md).


## Data Description:

Link to original Data Set on Kaggle: [Data Set.](https://www.kaggle.com/datasets/mmohaiminulislam/ecommerce-data-analysis) **Thanks** to [M Mohaiminul Islam](https://www.kaggle.com/mmohaiminulislam)

There are exactly 6 tables, 1 of which is a fact table and the rest are dimension tables.

 - Trans_dim  
 - customer_dim.    
 - fact_table
 - item_dim
 - store_dim 
 - time_dim

For more detalied information on Data Description go to [Data Preview](https://github.com/mfernandezcean/ECommerce_Data_Analysis/tree/main/Data_Preview)

- [Loaded](https://github.com/mfernandezcean/ECommerce_Data_Analysis/tree/main/Data_Loading) the CSV files into the created SQL Database. 

### [Schema](https://github.com/mfernandezcean/ECommerce_Data_Analysis/edit/main/Data_Schema/Readme.md):

![image](https://github.com/mfernandezcean/ECommerce_Data_Analysis/assets/105746149/bd1c6fe0-f08b-466b-86ea-0af420752ee2)


## [Data Exploration](%5BLoaded%5D%28https://github.com/mfernandezcean/ECommerce_Data_Analysis/tree/main/Data_Loading%29):

- Rows:

|  Table Name| num_rows |
|--|--|
| Customer Table |9,191|
| Fact Table| 1,000,000|
|Item Table | 264|
| Store Table|726 |
| Time Table|99,999 |
| Transaction (_payment_) Table| 39|


For more in depth information on Data Exploration, visit the [folder](https://github.com/mfernandezcean/ECommerce_Data_Analysis/edit/main/Data_Exploration/Readme.md)

## This important information has been gathered:

For much more detailed info go to the [Data_Queriyng folder](https://github.com/mfernandezcean/ECommerce_Data_Analysis/blob/main/Data_Querying/Readme.md)

 - Top Item: **Red Bull 12oz with 1,305,700 units**
 - Bottom Item: **Blue Diamond Almonds Rstd, Sltd with 136,908**
 
 - Top Supplier: **DENIMACH LTD From Bangladesh**
 - Bottom Supplier **CHERRY GROUP CO.,LTD From China**
 
 - Top Customer: **Pooja**
 - Bottom Customer: **Indrvati**

 - Top Year *(by income)* : **2018 with 15,108,197**
 - Bottom Year *(by income)*: **2014 with 14,334,731** *(excluding 2021)*

Top 3 Revenue Descriptions:

|  | Description | Income|
|--|--|--|
|1  | Beverage - Energy/Protein  |10,737,402
|  2| Food - Healthy |10,379,038
| 3 | Kitchen Supplies |8,434,526

Bottom 3 Revenue Descriptions:

|  | Description | Income|
|--|--|--|
|1  | Coffee K-Cups Tea  |201,186
|  2| Coffee Stirrers |386,461
| 3 | Dishware - Bowls |637,224
