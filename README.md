# Sales Insights – Brick & Motor Business | Power BI & SQL

## 1. Project Overview

This project focuses on developing an interactive and automated **Sales Analytics Dashboard** for AtliQ Hardware, a brick-and-mortar hardware business, using **MySQL and Microsoft Power BI**.

The primary objective is to transform raw sales data stored in a MySQL database into meaningful business insights through SQL-based data analysis, ETL (Extract, Transform, Load), data cleaning, data modeling, and interactive Power BI visualizations.

The dashboard enables business stakeholders, particularly the Sales Director, to monitor sales performance, identify regional trends, evaluate revenue patterns, and make informed, data-driven business decisions.

Instead of relying on inconsistent Excel reports and verbal updates from regional managers, the project provides a centralized reporting solution with accurate and structured sales information.

## 2. Business Problem Statement

AtliQ Hardware's Sales Director, Bhavin, observed a decline in overall sales performance but was unable to identify the underlying reasons.

The existing reporting system presented several challenges:

1. **Unreliable Reporting:** The Sales Director depended on Excel reports and verbal updates from regional managers. These reports were inconsistent, lacked meaningful insights, and sometimes did not match actual revenue figures.

2. **Lack of Centralized Information:** Sales information was distributed across different reports, making it difficult to obtain a consolidated view of business performance.

3. **Difficulty Identifying Sales Trends:** The existing reporting approach did not provide an effective way to identify declining sales, evaluate regional performance, or recognize potential growth opportunities.

4. **Need for Automated Reporting:** The Sales Director wanted an automated Power BI dashboard connected directly to the company's MySQL sales database to obtain accurate and up-to-date business insights.

### Proposed Solution

Develop an interactive Power BI dashboard connected to the MySQL database that:

- Automates the sales reporting process.
- Provides a centralized view of sales performance.
- Enables analysis of revenue trends and regional performance.
- Helps identify business opportunities and areas requiring improvement.
- Supports faster and more informed decision-making.

## 3. Project Objectives

The major objectives of this project are:

- Connect MySQL databases with Microsoft Power BI for seamless data integration.
- Perform exploratory data analysis using SQL queries.
- Implement the ETL process to extract, transform, clean, and load sales data.
- Identify and eliminate duplicate, invalid, and inconsistent transaction records.
- Standardize transaction currencies to enable consistent revenue analysis.
- Implement a Star Schema data model for efficient analytical reporting.
- Develop interactive dashboards to visualize sales trends and business performance.
- Provide actionable insights to support strategic sales decisions.

## 4. Technology Stack

| Category | Tools / Technologies |
|---|---|
| Database Management | MySQL |
| Data Analysis | SQL |
| Business Intelligence | Microsoft Power BI |
| Data Transformation | Power Query |
| Data Modeling | Star Schema |
| Data Visualization | Power BI Visualizations |
| Data Integration | MySQL – Power BI Connector |
| ETL | Extract, Transform, Load |

## 5. Dataset and Data Source

The project uses sales data from AtliQ Hardware, stored in a MySQL database.

The database contains business-related information required to analyze sales transactions, markets, and overall business performance.

The raw database was loaded using the provided `db_dump.sql` file.

### Data Source Workflow

1. Import the `db_dump.sql` file into MySQL.
2. Load the database and inspect the available tables.
3. Understand the relationships between the tables.
4. Execute SQL queries to explore and analyze the sales data.
5. Connect the MySQL database to Power BI for further transformation and visualization.

## 6. Project Workflow

The project follows an end-to-end data analytics workflow:

**MySQL Database → SQL Analysis → ETL → Data Cleaning → Star Schema → Power BI Dashboard → Business Insights**

### Step 1: Database Setup and SQL Analysis

- Installed and configured MySQL.
- Imported the `db_dump.sql` file to create and populate the database.
- Explored the available database tables and their relationships.
- Performed SQL-based analysis to understand the underlying sales data.
- Identified data quality issues that could affect revenue calculations and business reporting.

### Step 2: ETL – Extract, Transform, Load

Implemented the ETL process to prepare the raw database records for analytical reporting.

**Extract:**
- Connected to the MySQL database.
- Retrieved the required sales and business-related records.

**Transform:**
- Identified invalid and duplicate transactions.
- Removed records containing zero or negative sales amounts and quantities.
- Standardized transaction currencies.
- Excluded irrelevant geographical markets.
- Prepared and structured the data for analytical modeling.

**Load:**
- Loaded the cleaned and transformed data into Power BI.
- Prepared the data model for dashboard development and visualization.

### Step 3: Data Cleaning and Transformation

Data cleaning was an important part of the project because inaccurate transaction records and inconsistent currencies could distort the final revenue calculations.

The following transformations were performed:

- Identified and filtered invalid sales transactions.
- Removed duplicate records.
- Eliminated transactions with zero or negative sales amounts.
- Eliminated transactions with zero or negative sales quantities.
- Standardized different currencies into Indian Rupees (INR).
- Excluded non-India markets, such as New York and Paris, from the India-focused analysis.

### Step 4: Data Modeling – Star Schema

Designed a Star Schema data model to organize the sales data and establish relationships between the relevant tables.

The Star Schema provides a structured approach to analytical reporting by organizing data into fact and dimension tables.

This data modeling approach supports efficient data analysis and makes it easier to develop meaningful Power BI visualizations.

### Step 5: Power BI Integration

- Connected Microsoft Power BI directly to the MySQL database.
- Imported the required database records.
- Applied data transformation and cleaning using Power Query.
- Prepared the data model using the Star Schema.
- Established the necessary table relationships.
- Organized the cleaned data for dashboard development.

### Step 6: Interactive Dashboard Development

Developed an interactive Power BI dashboard to provide a consolidated view of AtliQ Hardware's sales performance.

The dashboard is designed to help stakeholders analyze business performance, monitor sales trends, identify growth opportunities, and support data-driven decisions.

## 7. Challenges Faced and Solutions Implemented

### Challenge 1: Dirty Data in the Transactions Table

**Problem:**

The transactions table contained several data quality issues, including:

- Zero sales amounts.
- Negative sales amounts.
- Zero sales quantities.
- Negative sales quantities.
- Duplicate transaction records.

These invalid records could lead to inaccurate revenue calculations and misleading business insights.

**Solution:**

- Used SQL queries to identify invalid transaction records.
- Filtered out transactions containing zero or negative sales amounts and quantities.
- Identified and removed duplicate records.
- Ensured that only valid transaction records were considered for further analysis.

### Challenge 2: Mixed Currencies

**Problem:**

The database contained transactions recorded in different currencies, including USD and INR.

Directly aggregating these values would result in inaccurate revenue calculations because the transactions were not expressed in a common currency.

**Solution:**

- Identified transactions recorded in different currencies.
- Used Power Query to standardize the currency values.
- Converted USD transactions into Indian Rupees (INR) using a currency conversion rate.
- Ensured that revenue calculations were performed using a consistent currency.

### Challenge 3: Non-India Markets in the Dataset

**Problem:**

The markets table contained geographical entries such as New York and Paris, which were not relevant to the India-focused sales analysis.

Including these markets could introduce irrelevant records into the analysis.

**Solution:**

- Examined the markets table to identify geographical inconsistencies.
- Identified non-India markets.
- Excluded irrelevant markets such as New York and Paris during data cleaning and modeling.
- Prepared the dataset for India-focused business analysis.

## 8. Business Insights and Impact

The developed dashboard provides stakeholders with a centralized and interactive platform for understanding sales performance.

The project aims to help the Sales Director and regional managers:

- Monitor overall sales performance.
- Analyze revenue trends.
- Evaluate sales performance across different markets.
- Identify declining sales patterns.
- Recognize potential growth opportunities.
- Make informed business decisions using data-driven insights.

The insights obtained from the dashboard can support the development of targeted sales strategies and improvement initiatives.

**Business Impact:**

The dashboard insights contributed to strategies projected to increase quarterly revenue by **7%**.

*Note: The 7% figure represents a projected revenue improvement from the proposed strategies, not a measured or confirmed revenue increase.*

## 9. Key Learnings

Through this project, I gained practical experience in:

- Working with relational databases using MySQL.
- Writing SQL queries for data exploration and analysis.
- Understanding and implementing the ETL process.
- Identifying and handling real-world data quality issues.
- Performing data transformation using Power Query.
- Handling multiple currencies in business datasets.
- Designing Star Schema data models.
- Integrating MySQL databases with Power BI.
- Developing interactive business intelligence dashboards.
- Translating raw business data into meaningful insights.
- Understanding how data analytics supports business decision-making.

## 10. Conclusion

This project demonstrates an end-to-end business intelligence solution using MySQL and Power BI to address real-world sales reporting challenges faced by AtliQ Hardware.

By integrating SQL-based data analysis, ETL operations, data cleaning, currency standardization, Star Schema modeling, and interactive Power BI dashboards, the project transforms raw sales data into meaningful business insights.

The developed solution reduces dependence on inconsistent manual reporting and provides stakeholders with a centralized platform to monitor sales performance, identify growth opportunities, and make informed business decisions.

Overall, this project highlights the practical application of SQL and Power BI in solving business analytics problems and supporting data-driven decision-making.




## 11. How to Run the Project

Follow these steps to reproduce the project:

### Prerequisites

- MySQL Server
- MySQL Workbench (recommended)
- Microsoft Power BI Desktop
- MySQL Connector/ODBC or the appropriate MySQL connector required by your Power BI installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/rajputporika02/Power-BI-X-SQL.git
```

```bash
cd Power-BI-X-SQL
```

### Step 2: Import the Database

1. Open MySQL Workbench.
2. Connect to your MySQL server.
3. Open the `db_dump.sql` file.
4. Execute the SQL script to create and populate the database.
5. Verify that the required tables have been imported successfully.

### Step 3: Perform SQL Analysis

1. Open the SQL scripts in MySQL Workbench.
2. Execute the required queries.
3. Explore the sales transactions and market-related tables.
4. Identify invalid records, duplicates, and inconsistent data.
5. Prepare the cleaned dataset for Power BI.

### Step 4: Connect MySQL to Power BI

1. Open Power BI Desktop.
2. Select **Get Data**.
3. Choose the MySQL database connector.
4. Enter the MySQL server and database details.
5. Select the required tables.
6. Import the data into Power BI.

### Step 5: Data Transformation and Modeling

1. Open Power Query Editor.
2. Apply the required data cleaning operations.
3. Standardize currencies into INR.
4. Exclude irrelevant markets.
5. Load the transformed data.
6. Establish relationships using the Star Schema data model.

### Step 6: Explore the Dashboard

Open the `.pbix` file using Power BI Desktop to interact with the sales analytics dashboard.

*Important: Update database connection credentials and paths according to your local MySQL configuration.*

## 12. Future Scope

The project can be extended through:

- Automated data refresh to keep business reports up to date.
- Integration of additional business datasets.
- Advanced sales forecasting using machine learning.
- More detailed customer and product-level sales analysis.
- Development of additional KPIs for monitoring business performance.
- Automated alerts for unusual sales declines.
- Deployment of dashboards through Power BI Service for wider stakeholder access.

## 14. Author

**Porika Abidsingh Rajput**

Integrated Dual Degree – Mechanical Engineering  
Indian Institute of Technology (BHU), Varanasi

**Areas of Interest:** Machine Learning | Data Analytics | Business Intelligence | SQL | Power BI

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.
