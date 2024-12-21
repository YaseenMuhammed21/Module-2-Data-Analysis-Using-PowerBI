# Data Analysis Using Power BI

## This assignment is about data transformation, visualization and analysis of a 'Financial Data of 'X'' using Power Query and Power BI

### Steps has been completed in the process.

1. Loaded the 'Financials' file into Power Query to transform and load into Power  BI for further process

2. Promoted the Headers

3. Removed the 'Null' values

4. Removed duplicates and blank rows

5. Removed the unwanted column('Manufacturing Price' column was incorrect in given data we have removed the same)

7. Removed column('Month Number', 'Month Name' and Year)

### DAX Operations

1. Created new tables 'Country Table', 'Date Table', 'Products Table', 'Sales By Country', 'Sales By Date', 'Sales By Products'

### Country Table
##
  Country Table = (DISTINCT(financials[Country]))

### Date Table
##
   Date Table = (DISTINCT(financials[Date]))

### Products Table
##
   Products Table = DISTINCT(financials[Product])

### Sales By Country
##
   Sales By Country = SUMMARIZE('Country Table','Country Table'[Country],"Total Sales",SUM(financials[Sales]),"Total Profit", SUM(financials[Profit]))

### Sales By Date
##
   SalesByDate = SUMMARIZE('Date Table','Date Table'[Date],"Total Sales",SUM(financials[Sales]),"Total Profit", SUM(financials[Profit]))
   
### Sales by Products
##
   Sales By Product = SUMMARIZE('Products Table','Products Table'[Product],"Total Sales",SUM(financials[Sales]),"Total Profit", SUM(financials[Profit]))

### Visualization

1. Created the visual for Performance By Person to get the visualization of individual Sale Person
2. Created the visual to study Market across the world
3. Created the visual to study the Shipment scenario across the sale
4. Created the visual for market drill down to know the area to increase the sale
5. Created the Summary for the project

## We have used Stacked Bar Chart, Clustered Column Chart, Card, Slicer, Map, Line and Clustered Column Chart, Tree Map, Matrix, Scatter Chart and Gauge Chart

