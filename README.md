# Intermediate-Assessment-Codeathon
Power BI – Module End Evaluation

# Data Cleaning and Loading

Imported the dataset into Power BI using Power Query Editor.

## Handling Missing Values

Identified missing values in Order Date, Customer  Name, Region, Product, Unit Price, Sales, Cost and Profit columns
* Order Date: Removed rows containing missing dates using the Remove Empty option.
* Customer Name, Region and Product: Replaced missing values with "Unknown".
* Unit Price, Sales, Cost and Profit: Added custom columns to calculate and replace missing values
  
Unit Price = Sales / Quantity

Sales = Quantity * Unit Price 

Cost = Sales – Profit 

Profit = Sales - Cost
## Removing Duplicate Rows
  Removing duplicate rows
  
•	Selected the dataset in Power Query Editor and Removed duplicate rows from the dataset

Home → Remove Rows → Remove Duplicates.
## Standardizing the Order Date Column
Standardizing the OrderDate column to a consistent date format.

•	Changed the data type of the Order Date column to Date.

•	Standardized the date format to DD-MM-YYYY.
## Loading the Cleaned Dataset
Load the cleaned dataset into the Power BI model.

•	Home → Close & Apply.

•	Loaded the cleaned dataset into the Power BI data model.
# Visualizations and Insights
Created a Pie Chart showing order distribution across different regions

* Legend: Region

* Values: Count of Order ID

Created a Column Chart to display the top 5 trending products based on the number of times each product was ordered.
* X-axis: Product
* Y-axis: Count of Order ID
* Applied Top N Filter:

1.	Opened the Filters 
3.	Selected the Product field.
4.	Changed the filter type to Top N.
5.	Selected Top 5 under Show Items
6.	Added Count of Order ID to the By Value field.
7.	Clicked Apply Filter.
   
Created a Line Chart to show the profit trend over time.
* X-axis: Order Date
* Y-axis: Sum of Profit
# DAX Calculations
Created a Calculated Table named EastRegionOrders that filters and displays only the orders from the East region.
* EastRegionOrders = FILTER('summative assigenment','summative assigenment'[Region]="East")
  
Created a Calculated Column to compute the difference between the Profit and Cost columns. Name it ProfitCostDifference.
* profit cost difference = 'summative assigenment'[adjusted cost]-'summative assigenment'[adjusted profit]
  
Created a Calculated Measure to find the total profit earned. Name it TotalProfit.
* total profit = sum('summative assigenment'[adjusted profit])





 




