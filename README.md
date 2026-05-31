# 🚀 Optimising E-commerce Discount Strategies to Balance Revenue and Brand Equity

### 📌 Project Overview
This project addresses a strategic conflict within a premium e-commerce company regarding whether promotional discounting drives sustainable growth or undermines the brand's "Quality Segment" positioning. By identifying a **"sweet spot" discounting tier of 10-20%**, I reconciled the Marketing Team's customer acquisition goals with the Board's demand for high profit margins and brand protection.

---
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white) 
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white) 
![Matplotlib](https://img.shields.io/badge/-Matplotlib-000000?style=flat&logo=matplotlib&logoColor=white) 
![Seaborn](https://img.shields.io/badge/-Seaborn-4A86A8?style=flat&logo=seaborn&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat&logo=postgresql&logoColor=white) 
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat&amp;logo=jupyter&amp;logoColor=white>)





### 📈 Key Findings & Results


* **The 10-20% "Sweet Spot"**: Discounts in the 10-20% range represent the company's primary financial engine, generating over €2.38M in revenue. This suggests that peak          revenue is most efficiently achieved at moderate discount levels.

* **Diminishing Returns on Deep Discounts**: Discounts exceeding 30% are associated with a marked decrease in both order volume and financial efficiency, contributing only        €0.57M to total revenue. This signals that extreme price cuts do not effectively incentivize higher unit sales and should be deployed only with specific strategic           intent.

* **Brand Value Stability**: The Average Order Value (AOV) trended upward from €120 to over €200 throughout the period. This suggests that targeted discounting has not            devalued the brand perception for core customers.

* **Seasonality and Revenue Drivers**: Peak holiday events (e.g., Black Friday/Christmas) drive revenue spikes up to 8x higher than average weeks. The analysis reveals a          positive correlation (r = 0.6469) between order volume and revenue, supporting the conclusion that transaction frequency is a primary growth driver.

* **Correlation between Discounts and Revenue**: The calculated correlation of r = 0.4826 between total discount and revenue suggests a moderate positive relationship. This       further confirms that revenue growth is driven by a complex mix of timing and demand rather than discounts alone.

* **Category-Specific Strategy**: Discounting requirements vary significantly by product type. Smartphones maintain consistent performance with an average discount of           11.05%,while Laptops show a higher average of 22.55%. This difference indicates a targeted strategy to liquidate refurbished or end-of-life inventory—such as older Mac      mini models—without impacting the premium status of high-end offerings.


  

  ### 📊 Data Insights & Visualizations

 
 
  #### 1. Growth & Correlation Analysis
 
 
   These charts settle the debate on whether promotions drive financial growth.

* The **sub plot** demonstrates that volume is a reliable driver of revenue, showing that even with discounts, total revenue rise consistently alongside the number of 
  products sold.
  
	
   <img src="Images/Volume-Revenue%20dual%20plot.png" width="600">

* The figure suggests order volume is closely related to revenue, a trend further supported by the average number of 1.12 items per order.
  
   <img src="Images/Weekly%20Revenue%20VS%20Order%20Volume.png" width="600">




 #### 2. Seasonality & Market Impact
 
 * Revenue spikes up to 8x higher during Black Friday and Christmas, confirming the necessity of a seasonal promotion calendar.



    <img src="Images/Weekly%20Revenue%20Impact%20Of%20Holiday%20Sales.png" width="600">

	

* "This comparison suggests that peak revenue is often achieved at controlled discount levels, supporting the existence of a 'sweet spot' for promotional intensity.


    <img src="Images/Monthly%20Revenue%20Vs%20Average%20Discount%20percentage.png" width="600">



#### 3. Brand Health & Category Strategy 

 * These charts support the strategy of protecting the brand's premium status while effectively managing stock levels

 * The increase in Average Order Value from €120 to over €200 suggests that targeted discounting has not devalued the brand for core customers, as reflected by the shift in    transaction value.


    <img src="Images/Monthly%20AOV.png" width="600">

 * The data suggests that Smartphones are maintained as a premium category through a controlled 11.05% discount, whereas the 22.55% average for Laptops supports a targeted     strategy to liquidate used and refurbished inventory without devaluing high-end models.

    <img src="Images/Average%20Discount%20Percentage%20By%20Category.png" width="600">


 * The data suggests that specific categories dominate revenue, supporting the strategy of prioritizing high-value segments to drive financial performance.

   <img src="Images/Total%20Revenue%20By%20Category.png" width="600">


   ### 💡Strategic Recommendations

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
```
E-commerce-Discount-Analysis/
├── cleaned dataset/              # Processed data for analysis
│   ├── brands.csv
│   ├── orderlines_cl.csv
│   ├── orders_cl.csv
│   └── products_cl.csv
├── Original Dataset(uncleaned)/  # Raw source files
│   ├── brands.csv
│   ├── orderlines.csv
│   ├── orders.csv
│   └── products.csv
├── images/                       # Generated visualisations
│   ├── Average Discount Percentage By Category.png
│   ├── Monthly AOV.png
│   ├── Monthly Revenue Vs Average Discount percentage.png
│   ├── Total Revenue By Category.png
│   ├── Volume-Revenue dual plot.png
│   ├── Weekly Revenue Impact Of Holiday Sales.png
│   └── Weekly Revenue VS Order Volume.png
├── 01_Data_cleaning.ipynb        # Data preparation notebook
├── 02_Data_analysis.ipynb        # Main analysis notebook
└── README.md                     # Project documentation
```

### 🛠 Environment & Tools
* **Development Environment:** Google Colab
* **Primary Language:** Python
* **Data Analysis & Visualization:** pandas, numpy, matplotlib, seaborn


### How to Use This Project


1.	**Main Analysis**: View the complete analysis in Data_Analysis.ipynb.
  
2.	**Run the Code**: Open the notebook in Google Colab and run all cells.
  
3.	**Dependencies**: Ensure you have imported the required libraries: import pandas numpy matplotlib seaborn.


## 👤 Contact & Connect
**Sruthi Raajan** 
* **LinkedIn:** https://www.linkedin.com/in/sruthi-raajan
* **GitHub Portfolio:** https://github.com/sruthi-raajan9
* **Email:** sruthiraajan9@gmail.com







	
