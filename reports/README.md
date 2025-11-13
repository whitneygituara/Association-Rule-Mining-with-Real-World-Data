Association Rule Mining Assignment 🛒✨
Author: Whitney Wairimu Gituara
Student ID: 528
Date: 13/11/2025
________________________________________
Project Overview 📊
This project explores association rule mining, a method used to discover patterns in large datasets, especially items often bought together.
Example: In a supermarket, if many customers buy bread and butter together, the store can:
•	Place these items near each other.
•	Offer promotions or discounts.
•	Suggest additional products online.
Objectives:
1.	Clean and organize the dataset for accurate analysis 🧹
2.	Identify frequent itemsets (items often bought together) 🔍
3.	Generate association rules with support, confidence, and lift 📈
4.	Visualize patterns to make them easy to understand 🎨
5.	Provide business insights from the rules 💡
________________________________________
Dataset Description 🗂️
Name: retail_store_sales.csv
Source: Kaggle - ( https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning?resource=download )
Column Name	Description
Customer ID	Unique identifier for each customer
Transaction ID	Unique identifier for each transaction
Category	Category of the purchased item (e.g., Milk Products, Beverages)
Item	Name of the purchased item
Price Per Unit	Price of one unit of the item
Quantity	Number of units bought
Total Spent	Total amount spent on the transaction
Discount Applied	Discount applied on the transaction
________________________________________
Libraries Used 📚
Library	Purpose
pandas	Load, clean, and organize data
numpy	Perform mathematical calculations
mlxtend	Generate frequent itemsets and association rules
matplotlib	Create charts and visualizations
seaborn	Advanced visualizations
collections	Count occurrences of items (used for plotting antecedents)
________________________________________
Step-by-Step Methodology 🧩
Step 1: Data Cleaning 🧹
•	Removed rows with missing items
•	Filled missing numeric values with 0
•	Removed duplicate rows
•	Normalized item names:
o	Converted to lowercase
o	Removed leading/trailing spaces
o	Extracted meaningful part after last underscore (e.g., Item_10_PAT → pat)
This is to ensure accurate and consistent data.
________________________________________
Step 2: Preparing Transactions 🛒
•	Grouped by Transaction ID → baskets of items bought together
•	Grouped by Customer ID → all items a customer bought over time
This is because the algorithms need lists of items per transaction.
________________________________________
Step 3: One-Hot Encoding 🔢
•	Converted items to 1s (bought) and 0s (not bought)
•	Each row = one transaction/customer
•	Each column = one item
This is because algorithms like Apriori require numeric input.
________________________________________
Step 4: Frequent Itemset Mining 🔍
•	Applied Apriori algorithm
•	Minimum support = 1%
•	Sorted by support to find most common item combinations
Visualization:
•	Bar chart for Top 10 frequent itemsets
________________________________________
Step 5: Generating Association Rules 📈
•	Lowered support = 0.5% for customer-level transactions
•	Minimum confidence = 10%
•	Filtered rules:
o	Antecedent and consequent must have ≥1 item
o	Total items (antecedent + consequent) ≥ 2
•	Sorted by lift (how much more likely items occur together than by chance)
________________________________________
Step 6: Customer Item Frequency Visualization 🎨
•	Counted how many customers purchased each item
•	Plotted Top 10 items purchased by customers
________________________________________
Step 7: Top 4 Interesting Rules ✨
•	Picked top 4 rules by lift
•	Displayed:
o	Antecedent → triggers the rule
o	Consequent → likely next item bought
o	Support, confidence, lift
Example:
Customers who buy milk also tend to buy butter, with a confidence of 80% and lift of 1.5
Bar chart: Frequency of antecedents in top 4 rules
________________________________________
Step 8: Business Insights 💡
•	Identify items often bought together → cross-selling opportunities
•	Improve product placement in stores
•	Understand customer preferences and buying patterns
________________________________________
Sample Outputs 🖼️
•	Bar chart: Top 10 frequent itemsets
•	Bar chart: Top 10 items purchased by customers
•	Top 4 association rules with support, confidence, and lift
________________________________________
GitHub Repository Structure 🗄️
/data/        → retail_store_sales.csv
/notebooks/   → Jupyter notebook with all code
/plots/       → plots
README.md
report.md or report.pdf

________________________________________
Google Colab Notebook 📖
You can explore the full implementation and run the code directly here:
https://colab.research.google.com/drive/1aYC8_TOepAk9zTrVmAu76d75cuaCgbHd?usp=sharing 


