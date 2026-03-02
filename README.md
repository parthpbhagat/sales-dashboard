# Sales & Customer Performance Dashboard 📊

## Project Overview
This project is an interactive Power BI dashboard designed to analyze retail sales, track customer performance, and monitor product returns. By leveraging a structured Star Schema data model, it provides actionable insights into revenue generation, regional performance, and return trends to help drive data-driven business decisions.

## Dataset
The analysis is built on a relational dataset consisting of Fact and Dimension tables:
* **Dimension Tables:**
  * `Customer_Dim.csv`: Customer details, segments (Consumer, Corporate, Home Office), and regions.
  * `Product_Dim.csv`: Product hierarchy (Category, SubCategory) and pricing.
  * `Region_Dim.csv`: Geographical regions and their respective managers.
  * `Date_Dim.csv`: Time dimension containing Year, Quarter, Month, and Date.
* **Fact Tables:**
  * `Sales_Fact.csv`: Core sales transactions including Units Sold and Total Amount.
  * `Returns_Fact.csv`: Records of returned orders along with return reasons (e.g., Late Delivery, Defective, Wrong Item).

## Data Model
The project utilizes a **Star Schema** to establish relationships between the tables. The `Sales_Fact` and `Returns_Fact` tables are logically connected to the descriptive dimension tables via primary and foreign keys (such as `CustomerID`, `ProductID`, `DateID`, and `SaleID`).

## Key Performance Indicators (KPIs) & Insights
* **Total Revenue:** Overall sales amount generated.
* **Total Units Sold:** Volume of products sold across different categories.
* **Total Orders:** Count of unique sales transactions.
* **Return Rate:** Percentage of returned orders vs. total orders.
* **Return Reason Analysis:** Breakdown of why products are returned to identify operational bottlenecks (e.g., fixing late deliveries).
* **Customer Segmentation:** Sales performance split by different customer types.

## Tools & Technologies Used
* **Power BI Desktop:** For Data Visualization and Dashboard creation.
* **Power Query Editor:** For Data Cleaning, merging columns, and Data Transformation.
* **DAX (Data Analysis Expressions):** For building custom measures and calculations (e.g., Return Rate, Total Revenue).

## How to Open and Use
1. Clone or download this project folder containing the `.csv` files and the `.pbix` file.
2. Open the `sales & Customer Performance dashboard.pbix` file using Power BI Desktop.
3. If the data visuals show an error regarding missing data, go to **Transform Data > Data Source Settings** and update the file paths to point to the local `.csv` files on your machine.
4. Use the provided slicers and filters on the dashboard pages to interact dynamically with the data.
