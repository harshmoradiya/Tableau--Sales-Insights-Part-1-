Tableau Sales Insights - Part 1

Why Tableau? 
"A Picture is Worth a Thousand Words"

This is a real-life dynamic data project based on sales insights. This project guides you step-by-step on how to perform tasks or work as an intern in any firm. From meetings to creating dashboards of insights, I will guide you through the entire process.

Step 1: Problem Statement
ATLIQ, a hardware company, wants to understand its performance in various areas such as sales, profit, and manufacturing. The company initiates a meeting to discuss this.

AIMS GRIDS
- Purpose**: To understand how the company is functioning in various criteria such as sales, profit, and manufacturing.
- Stakeholders**: Sales team, IT team, Data analytics team
- Result (Success Criteria)**: Clear insights into the company’s performance in the discussed areas.

Data Source
We have data from an OLTP (Online Transaction Processing) system, which is a critical system where day-to-day sales are recorded. This data will be analyzed using an OLAP (Online Analytical Processing) system.

Data Preparation
We will use SQL for ETL (Extract, Transform, Load) and data cleaning processes.

SQL Data Preparation
- Dimensions**: Order date, product ID, product name, etc.
- Measures**: Sales, profit, etc., which are countable.

Methodology
- Star Schema**: A central table (transaction table) where all other tables are connected via foreign keys. The transaction table includes fields such as order date, product ID, user ID, and market customer.

Data Cleaning
1. Removing Blank Spaces in Sales Amount**:
   - Navigate to Data -> Edit -> Data Source Filters
   - Add a filter on the sales amount to remove blank spaces.

2. Handling Currency Conversion**:
   - Convert minor amounts in USD to INR using a calculated field:
   sql
   IF [currency] == 'USD' THEN [sales amount] * 84 ELSE [sales amount] END
   

Creating Sheets and Dashboard in Tableau
1. Total Revenue**: 
   - Drag the normalized amount into marks and display it as text.

2. Sales Quantity**: 
   - Drag the sum of sales quantity into marks and display it as text.

3. Revenue by Market**:
   - Drag the market name into columns and the sum of the normalized amount into rows.

4. Sales Quantity by Market**:
   - Drag the market name into columns and the sum of sales quantity into rows.

5. Top 5 Customers by Revenue**:
   - Drag the customer name into columns and the sum of the normalized amount into rows.

6. Revenue by Year**:
   - Drag the month (from the order date) into columns and the sum of the normalized amount into rows.

Conclusion
After data cleaning, we create individual sheets and then combine them into a dashboard. The final dashboard will provide clear insights into total revenue, sales quantity, revenue by market, sales quantity by market, top 5 customers by revenue, and revenue by year.

What's Next?
In the next part, we will review the feedback from higher authorities after they have reviewed this dashboard and conducted a meeting. Based on their feedback, we will make necessary changes to our dashboard. So, stay tuned for Part 2. See you all soon!

I have uploaded screenshots of the output and the data files in the above repository. Thank you for reading this tutorial. Good luck, and stay connected for more such information!

