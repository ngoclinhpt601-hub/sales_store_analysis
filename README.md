# SQL Project: Sales Store Analysis

## Store Background
A retail store chain tracks daily sales transactions, including order details, customer info, product categories, order times, and order status. The business wants to optimize operations, improve customer experience, and increase profitability using data-driven decisions.

## Problem Statement
The store does not have a clear idea about :-
Which products sell the most,
Customers preference,
Which items bring in the most profit,and
Where things are going wrong indelivery or operations. 
Because of this, they are missing chances to earn more, losing customers, and making poor business decisions.

## 🎯 Project Objective
Analyze transactional sales data to:
- Identify top-selling products and categories.
- Understand customer behavior (VIPs, age groups, gender).
- Discover sales trends over time.
- Provide actionable insights for marketing, inventory, and customer retention strategies.

## ⚙️ Process Overview
1. **ETL (Extract – Transform – Load)**  
   - Imported CSV data into SQL Server using `BULK INSERT`.  
   - Created `sales_store` table with schema covering transactions, customers, products, payments, and status.  

2. **Data Cleaning**  
   - Removed **duplicates** using `ROW_NUMBER()` in CTE.  
   - Standardized column names with `sp_rename`.  
   - Checked and handled **NULL values** using dynamic SQL.  
   - Deleted **outliers** (e.g., missing transaction IDs).  
   - Normalized categorical values:  
     - Gender: `Male → M`, `Female → F`.  
     - Payment mode: `CC → Credit Card`.  
   - Corrected inconsistent records (customer IDs, age, gender).  

3. **Business Analysis Queries**
   - **Top 5 best-selling products** → prioritize inventory and promotions.  
   - **Top 5 most cancelled products** → improve product quality or remove from catalog.  
   - **Peak purchase times** (Morning, Afternoon, Evening, Night) → optimize staffing and server load.  
   - **Top 5 highest-spending customers** → design loyalty programs and personalized offers.  
   - **Revenue by product category** → invest in high-margin or high-demand categories.  
   - **Cancellation/return rates per category** → monitor dissatisfaction and logistics issues.  
   - **Preferred payment modes** → streamline payment processing.  
   - **Purchasing behavior by age group** → targeted marketing campaigns.  
   - **Monthly sales trends** → plan inventory and seasonal promotions.  
   - **Gender-based product preferences** → personalized ads and gender-focused campaigns.
     
### Key Results
- **Top 5 Products by Quantity Sold**: Wardrobe, Vegetables, Sofa, Dining Table, Fruits.  
- **Top 5 VIP Customers by Spending**: The amount they spent is around $99,000 or more.
- **Monthly Sales Trend**: Peak in July, lowest in May.  
- **Preferred Payment Mode**: Credit Card (32.4%), EMI (17.5%), Debit Card (17.2%).  
- **Age Group Spending**: 36-50 contributes the highest revenue share. 

## 📊 Key Insights
- **Top-selling products** drive majority of revenue → focus marketing efforts here.  
- **VIP customers** represent a small group but contribute significantly to total sales.  
- **Seasonal trends** show clear peaks → inventory planning is critical.  
- **Age and gender segmentation** enables more effective targeted marketing.  
- **Credit Card** is the most preferred payment mode → optimize payment systems accordingly.  
  
## 📈 Business Impact
This project demonstrates how SQL can be leveraged to:
- Optimize product portfolio and inventory management.  
- Build customer loyalty programs for high-value clients.  
- Personalize marketing strategies based on demographics and behavior.  
- Reduce cancellations/returns and improve customer satisfaction.

## 🛠️ Tools & Technologies
- SQL Server 2022  
- CSV dataset  
- GitHub for version control and documentation

 
