# 🚀 Optimising E-commerce Discount Strategies to Balance Revenue and Brand Equity

### 📌 Project Overview
This project addresses a strategic conflict within a premium e-commerce company regarding whether promotional discounting drives sustainable growth or undermines the brand's "Quality Segment" positioning. By identifying a **"sweet spot" discounting tier of 10-20%**, I reconciled the Marketing Team's customer acquisition goals with the Board's demand for high profit margins and brand protection.

---
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white) 
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white) 
![Matplotlib](https://img.shields.io/badge/-Matplotlib-000000?style=flat&logo=matplotlib&logoColor=white) 
![Seaborn](https://img.shields.io/badge/-Seaborn-4A86A8?style=flat&logo=seaborn&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat&logo=postgresql&logoColor=white) 
![Tableau](https://img.shields.io/badge/-Tableau-E97627?style=flat&logo=tableau&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat&amp;logo=jupyter&amp;logoColor=white>)





### 📈 Key Findings & Results


* **The 10-20% Sweet Spot** :  Discounts in the 10-20% range are the company's primary financial engine, generating over €2.38M in revenue.

* **Diminishing Returns on Deep Discounts** : Discounts exceeding 30% suffer a significant drop in both order volume and financial efficiency, contributing only €0.57M to 
    total revenue. This proves that extreme price cuts fail to incentivise higher unit sales and should be strictly limited.

* **Brand Value Remains Strong** :Despite the use of discounts, the Average Order Value (AOV) trended upward from €120 to over €200, proving that promotional activity did 
    not cheapen the brand in the eyes of consumers.

* **Seasonality is Critical**:Peak holiday events (Black Friday/Christmas) drive revenue spikes up to 8x higher than average weeks, confirming the necessity of a seasonal 
    discount strategy.

* **Category-Specific Strategy**  :  Discounting requirements vary significantly by product type. While Smartphones maintain strong sales with lower average 
discounts 11.05%, Laptops and Computers show a higher average discount of 22.55%. My analysis reveals this is driven by a high volume of Used/Refurbished units and End-
of-Life inventory (such as older Mac mini models), which require aggressive price cuts (>30%) to liquidate. Over half of the products in this category are sold with at 
least a 13% discount, primarily to move these non-new items. Meanwhile, Accessories act as "customer hooks," utilizing aggressive discounts (25%+) to drive the traffic 
necessary for overall brand growth. 


  

  ### 📊 Data Insights & Visualizations

 
 
  #### 1. Growth & Correlation Analysis
 
 
 These charts settle the debate on whether promotions drive financial growth.

* The **sub plot** demonstrates that volume is a reliable driver of revenue, showing that even with discounts, total revenue rise consistently alongside the number of 
  products sold.

	
   <img src="Images/Volume-Revenue%20dual%20plot.png" width="600">


   <img src="Images/Weekly%20Revenue%20VS%20Order%20Volume.png" width="600">




 #### 2. Seasonality & Market Impact
 
 * Revenue spikes up to 8x higher during Black Friday and Christmas, confirming the necessity of a seasonal promotion calendar.



    <img src="Images/Weekly%20Revenue%20Impact%20Of%20Holiday%20Sales.png" width="600">

	

* This comparison shows that peak revenue is often achieved at controlled discount levels, suggesting a "sweet spot" for promotional intensity.


    <img src="Images/Monthly%20Revenue%20Vs%20Average%20Discount%20percentage.png" width="600">



#### 3. Brand Health & Category Strategy 

 * These charts provide the evidence needed to protect the brand's premium status while clearing stock.

 * The increase in Average Order Value from €120 to over €200 proves that discounting has not devalued the brand for  core customers.


    <img src="Images/Monthly%20AOV.png" width="600">

 * This plot highlights Smartphones as a premium category maintained with a controlled 11.05% discount. In contrast, the 22.55% average seen in Laptops reflects a            targeted strategy to liquidate used and refurbished inventory without devaluing the new, high-end models

    <img src="Images/Average%20Discount%20Percentage%20By%20Category.png" width="600">


 * The bar chart showing which categories bring in the most total revenue.

   <img src="Images/Total%20Revenue%20By%20Category.png" width="600">


   ## Strategic Recommendations

  To optimize the balance between growth and brand protection, I recommend the following actions:

1. **Standardize the 10-20% Tier**: Establish this as the default promotional range to protect margins.

2. **Restrict Deep Discounts**: Since discounts above 30% show a clear drop in financial efficiency, the company should strictly limit these deep price cuts, reserving them only for end-of-life clearance.

3. **Segmented Pricing**: Apply the lower-tier discounts to premium categories like Smartphones to maintain brand equity, while utilizing the higher 20% range for Refurbished products to move inventory efficiently.




### 🧹 Data Cleaning & Methodology

To ensure the analysis was based on reliable data, the raw dataset underwent the following cleaning and refinement process:


* **Defining Realized Revenue**: The raw dataset contained 293,983 orderlines, including cancelled, abandoned, and unpaid orders. I filtered this down to only 'Completed' transactions to ensure findings represent actual money in the bank.

* **Data Integrity**: This process resulted in a high-integrity dataset of approximately 53,231 validated rows. By focusing on completed orders, the analysis reflects genuine customer behavior rather than "cart activity."

* **Discount Validation**: I identified and removed invalid orders (such as those with negative discount values) to ensure price elasticity calculations were 100% accurate.

* **Data Consolidation**: Information from Products, Orders, and Brands was merged to create a master "expanded" table, allowing for deep-dive analysis by category.


### 📂 Dataset & Sources

* **Source:** Internal Company E-commerce Database.
* **Dataset Size:** Over 293,000 raw orderlines spanning one fiscal year.
* **Key Features:** `id_order`, `sku`, `unit_price`, `product_quantity`, `date`, `category`, `brand`, `discount`.
* **Feature Engineering:** To deepen the analysis, the following columns were calculated:
    * `revenue`: Total value after applying discounts.
    * `total_discount`: Monetary value of the applied discount.
    * `percentage_discount`: Ratio of discount to unit price for elasticity analysis.

### Project Structure

**•	data** :  Contains the raw and cleaned CSV datasets .

**•	images** : Contains the generated visualisations used in the analysis.

**•	discount_analysis.ipynb** : The main Jupyter Notebook containing all data cleaning, exploration, and visualisations.

**•	README.md**: Project summary and findings.


### 🛠 Environment & Tools
* **Development Environment:** Google Colab
* **Primary Language:** Python
* **Data Analysis & Visualization:** pandas, numpy, matplotlib, seaborn


### How to Use This Project


1.	**Main Analysis**: View the complete analysis in Data_Analysis.ipynb.
  
2.	**Run the Code**: Open the notebook in Google Colab and run all cells.
  
3.	**Dependencies**: Ensure you have imported the required libraries: import pandas numpy matplotlib seaborn.







	
