# E-commerce-Discount-Analysis

A data-driven analysis to resolve a corporate debate on overall discounting strategies. This project investigates whether discounts drive sustainable revenue growth or undermine the brand's 'Quality Segment' positioning and total financial performance.

## Optimising E-commerce Discount Strategies to Balance Revenue and Brand Equity

## Project Overview

This project addresses a strategic conflict within a premium e-commerce company regarding whether promotional discounting drives sustainable growth or undermines the
brand's "Quality Segment" positioning. By analysing transaction data, I evaluated the relationship between discount intensity, order volume, total revenue, and average 
order value. I identified a "Sweet Spot" discounting tier that successfully reconciles the Marketing Team's customer acquisition goals with the Board's demand for high 
profit margins and brand protection.


### Data Cleaning & Methodology

To ensure the analysis was based on reliable data, the raw dataset underwent the following cleaning and refinement process:


**Defining Realized Revenue**: The raw dataset contained 293,983 orderlines, including cancelled, abandoned, and unpaid orders. I filtered this down to only 'Completed' transactions to ensure findings represent actual money in the bank.

**Data Integrity**: This process resulted in a high-integrity dataset of approximately 53,231 validated rows. By focusing on completed orders, the analysis reflects genuine customer behavior rather than "cart activity."

**Discount Validation**: I identified and removed invalid orders (such as those with negative discount values) to ensure price elasticity calculations were 100% accurate.

**Data Consolidation**: Information from Products, Orders, and Brands was merged to create a master "expanded" table, allowing for deep-dive analysis by category.


### Dataset & Sources


**Source**: Internal Company E-commerce Database.

**Size**: Over 293,000 raw orderlines spanning one fiscal year.

**Key Features**: id_order, sku, unit_price, product_quantity, date, category, brand, discount.

**Calculated Fields**: To deepen the analysis, I engineered revenue, total_discount, and percentage_discount columns.



### Key Findings & Results


**•	The 10-20% Sweet Spot** :  Discounts in the 10-20% range are the company's primary financial engine, generating over €2.38M in revenue.

**•	Diminishing Returns on Deep Discounts** : Discounts exceeding 30% suffer a significant drop in both order volume and financial efficiency, contributing only €0.57M to 
total revenue. This proves that extreme price cuts fail to incentivise higher unit sales and should be strictly limited.

**•	Brand Value Remains Strong** :Despite the use of discounts, the Average Order Value (AOV) trended upward from €120 to over €200, proving that promotional activity did 
not cheapen the brand in the eyes of consumers.

**•	Seasonality is Critical**:Peak holiday events (Black Friday/Christmas) drive revenue spikes up to 8x higher than average weeks, confirming the necessity of a seasonal 
discount strategy.

**•	Category-Specific Strategy**  :  Discounting requirements vary significantly by product type. While Smartphones maintain strong sales with lower average 
discounts 11.05%, Laptops and Computers show a higher average discount of 22.55%. My analysis reveals this is driven by a high volume of Used/Refurbished units and End-
of-Life inventory (such as older Mac mini models), which require aggressive price cuts (>30%) to liquidate. Over half of the products in this category are sold with at 
least a 13% discount, primarily to move these non-new items. Meanwhile, Accessories act as "customer hooks," utilizing aggressive discounts (25%+) to drive the traffic 
necessary for overall brand growth. 



### Technologies Used

**•	Programming** : Python

**•	Libraries** : pandas, numpy, matplotlib, seaborn

**•	Environment** : Google Colab Notebook


### Project Structure

**•	data** :  Contains the raw and cleaned CSV datasets .

**•	images** : Contains the generated visualisations used in the analysis.

**•	discount_analysis.ipynb** : The main Jupyter Notebook containing all data cleaning, exploration, and visualisations.

**•	README.md**: Project summary and findings.




 ### Visualisations

 
 
#### 1. Growth & Correlation Analysis
 
 
These charts settle the debate on whether promotions drive financial growth.

The dual-axis plot demonstrates that volume is a reliable driver of revenue, showing that even with discounts, total earnings rise consistently alongside the number of 
products sold.

	
<img src="Images/Volume-Revenue%20dual%20plot.png" width="600">


A near-perfect positive correlation  between order volume and revenue proves that driving volume is the primary engine for scaling.


<img src="Images/Weekly%20Revenue%20VS%20Order%20Volume.png" width="600">




#### 2. Seasonality & Market Impact
 
Revenue spikes up to 8x higher during Black Friday and Christmas, confirming the necessity of a seasonal promotion calendar.



<img src="Images/Weekly%20Revenue%20Impact%20Of%20Holiday%20Sales.png" width="600">

	

This comparison shows that peak revenue is often achieved at controlled discount levels, suggesting a "sweet spot" for promotional intensity.


<img src="Images/Monthly%20Revenue%20Vs%20Average%20Discount%20percentage.png" width="600">



#### 3. Brand Health & Category Strategy 

These charts provide the evidence needed to protect the brand's premium status while clearing stock.

The increase in Average Order Value from €120 to over €200 proves that discounting has not devalued the brand for  core customers.


<img src="Images/Monthly%20AOV.png" width="600">

This plot highlights Smartphones as a premium category maintained with a controlled 11.05% discount. In contrast, the 22.55% average seen in Laptops reflects a targeted strategy to liquidate used and refurbished inventory without devaluing the new, high-end models

<img src="Images/Average%20Discount%20Percentage%20By%20Category.png" width="600">


The bar chart showing which categories bring in the most total cash.

<img src="Images/Total%20Revenue%20By%20Category.png" width="600">


## Strategic Recommendations

To optimize the balance between growth and brand protection, I recommend the following actions:

**Standardize the 10-20% Tier**: Establish this as the default promotional range to protect margins.

**Restrict Deep Discounts**: Since discounts above 30% show a clear drop in financial efficiency, the company should strictly limit these deep price cuts, reserving them only for end-of-life clearance.

**Segmented Pricing**: Apply the lower-tier discounts to premium categories like Smartphones to maintain brand equity, while utilizing the higher 20% range for Refurbished products to move inventory efficiently.


### How to Use This Project


1.	**Main Analysis**: View the complete analysis in Data_Analysis.ipynb.
  
2.	**Run the Code**: Open the notebook in Google Colab and run all cells.
  
3.	**Dependencies**: Ensure you have imported the required libraries: import pandas numpy matplotlib seaborn.







	
