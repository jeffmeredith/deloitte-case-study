# deloitte-case-study
Proposing recommendations to Deloitte practitioners, boosting revenue and cutting losses through Demand Forecasting models.

## Dataset
Each team was given the same ECommerce dataset for the case study, containing 6 different data tables.
* customer_dim.csv - Contains data about each unique customer that has purchased from a store.
* item_dim.csv - Data about each item offered in all stores.
* store_dim.csv - Data about each store location.
* time_dim.csv - Data about the time of each transaction, down to the minute.
* trans_dim.csv - Data about all banks used by customers.
* fact_table.csv - A table of all keys from the other 5 data tables, each row representing a transaction.

## EDA
![Alt Text](plots/monthly_rev1.png)
![Alt Text](plots/monthly_rev2.png)
![Alt Text](plots/monthly_rev3.png) <br>
Found that significant low-point in sales always occurs during February, and peaks tend to happen between the months of August and December.
![Alt Text](plots/monthly_for_all_items.png) <br>
Found that month-to-month fluctuations were different for different item types.
![Alt Text](plots/sankey_products.png) <br>
Also considered product bundling as a business recommendation, showing common customer journeys through different products.

## Solution and Results
Developed three regression models, all with similar performance to predict month-to-month demands of different product types.
**Features:**
* Month (Categorical)
* Product Category
**Models:**
* Decision Tree Regressor: **R<sup>2</sup>: 0.97**
* XGBoost: **R<sup>2</sup>: 0.97**
* Long Short-Term Memory (NN): **R<sup>2</sup>: 0.99**
![Alt Text](plots/monthly_by_item.png)
