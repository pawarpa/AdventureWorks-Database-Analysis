# Retail Store Analysis: Data Warehousing and Business Intelligence

## A research question or challenge
The primary challenge of this project was to design and implement effective data warehousing and business
intelligence solution for a retail store dataset, i.e., AdventureWorks LT Dataset. The research question was centered on
around how to create a system that could efficiently handle the warehousing of retail data and provide insightful
business intelligence for decision-making.

## My approach and methodology
Tools: SQL, Talend, SSMS, MS Azure, ER Studio, Tableau, Power BI

-Data Integration and Warehouse: The project involved the integration of data from various sources within the retail
store, including sales data, inventory data, customer data, and product data. Data extraction and transformation
processes were employed to ensure data compatibility and consistency. The core of the project was the design and
creation of a data warehouse. A star schema was chosen to model the data, with fact and dimension tables. Slowly
Changing Dimension Type 2 (SCD2) was implemented for the Product Price History dimension to track historical
prices effectively.

-SCD Implementation: SCD2 is a method used to capture and manage historical changes to dimension data over
time. It is particularly useful when there is a need to track historical changes to specific attributes of dimension
tables, such as the Product Price History dimension in this project. The dimension table included attributes such as
the product ID, price, effective date (start date), and end date. The effective date represents the point in time
when a new price becomes active, and the end date represents the point in time when the previous price is no
longer valid. These date attributes are crucial for tracking the historical changes in product prices. When a new
price is recorded for a product, a new record is added to the Product Price History dimension table. The new record
includes the updated price, the effective date (start date), and an "end date" value of '9999-12-31' (or any future
date representing the end of the current price's validity). When a change occurs, the existing historical record's end
date is updated to the day before the effective date of the new record. This ensures that there is no overlap
between historical price records. In essence, the end date of the previous record becomes the day before the new
price's effective date. By implementing SCD2 in this manner, the data warehouse can retain the historical context
of product prices. This means that at any point in time, it is possible to query the data warehouse and retrieve the
price that was in effect for a product during a specific date range. This historical context is invaluable for reporting
and analysis. It allows users to track how product prices have evolved over time and analyze the impact of price
changes in sales and make informed decisions about pricing strategies and promotions.

-Business Intelligence: Using Tableau, interactive dashboards were designed to facilitate data visualization and
provide insights into product sales, customer behaviour, and overall store performance. Global filters were
incorporated for efficient data exploration.

## Findings and their significance
1. Comprehensive Data Integration: The successful integration of data from multiple sources provided a holistic view
of retail operations. This was vital for understanding customer behaviour, product performance, and sales trends.
2. Efficient Data Warehousing: The implemented data warehouse follows a star schema with SCD2 for historical
prices, allowed for the efficient storage and retrieval of retail data. This structure was vital for generating historical
insights.
3. Data-Driven Decision-Making: The interactive Tableau dashboards provided a user-friendly interface for store
management and analysts to explore and visualize the data. This empowers data-driven decision-making by offering
insights into products, customers, and sales.
4. Historical Analysis: The ability to track product price history and analyse historical data trends was significant for
making pricing decisions, assessing the impact of promotions, and optimizing inventory management.
5. KPI Monitoring: The dashboards allowed for the monitoring of key performance indicators (KPIs) related to
products, customers, and sales. This helped in identifying areas for improvement and setting performance benchmarks.
6. Efficient Resource Allocation: The insights derived from the project's business intelligence component could be
used for more efficient allocation of resources, such as inventory, marketing, and staffing.
