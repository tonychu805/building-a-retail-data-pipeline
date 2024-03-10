# building-a-retail-data-pipeline

Walmart is the biggest retail store in the United States. Just like others, they have been expanding their e-commerce part of the business. By the end of 2022, e-commerce represented a roaring $80 billion in sales, which is 13% of total sales of Walmart. One of the main factors that affects their sales is public holidays, like the Super Bowl, Labour Day, Thanksgiving, and Christmas.
![walmartecomm](https://github.com/tonychu805/building-a-retail-data-pipeline/assets/13603908/7f5a6c83-ef1f-4fb1-adce-a75a24d8c9e8)
In this project, I created a data pipeline for the analysis of supply and demand around the holidays, along with conducting a preliminary analysis of the data. There are two data sources: grocery sales and complementary data.


grocery_sales
- "index" - unique ID of the row
- "Store_ID" - the store number
- "Date" - the week of sales
- "Weekly_Sales" - sales for the given store

extra_data.parquet
- "IsHoliday" - Whether the week contains a public holiday - 1 if yes, 0 if no.
- "Temperature" - Temperature on the day of sale
- "Fuel_Price" - Cost of fuel in the region
- "CPI" – Prevailing consumer price index
- "Unemployment" - The prevailing unemployment rate
- "MarkDown1", "MarkDown2", "MarkDown3", "MarkDown4" - number of promotional markdowns
- "Dept" - Department Number in each store
- "Size" - size of the store
- "Type" - type of the store (depends on Size column)

The expected output shall be a merged file containing the following columns:

- "Store_ID"
- "Month"
- "Dept"
- "IsHoliday"
- "Weekly_Sales"
- "CPI"
- ""Unemployment""

Finally, after merging and cleaning the data, summarize the average monthly sales.
