
#  **Warehouse-And-Retail-Sales and Data Exploration**  

![Warehouse Sales GIF](https://images.squarespace-cdn.com/content/v1/5f998d41303db018cd809687/16bdb895-eaad-4beb-a60f-fe0fb1d02c0d/Row-of-colorful-wine-bottles-sitting-in-front-of-a-textured-green-gray-wall.jpg)   

---

## 📝 **Project Overview**  

This project focuses on clustering products using **historical sales data** to optimize **inventory management**, identify **market trends**, and tailor **product offerings**.

---

## 🎯 **Goals and Objectives**  

### 🚦 **Goals**:  
1. **Optimize Inventory**: Prevent overstocking/understocking.  
2. **Empower Insights**: Drive decisions in marketing and sales.  
3. **Competitive Edge**: Stay ahead using data-driven analysis.  

###  **Objectives**:  
-  Conduct clustering analysis to group similar products.  
-  Create insightful visualizations and dashboards.  
-  Document methodology for reproducibility.  

---

## 🛠 **Key Features**  

| 🏷️ **Feature**             | 🧩 **Details**                                                                 |
|-----------------------------|------------------------------------------------------------------------------|
| 📅 **Time Frame**           | Analyzes data from **2017–2020**.                                             |
| 🔍 **Clustering Approach**  | Uses sales **patterns and attributes** to group products.                    |
| 📈 **Exploratory Analysis** | Trends on **Sales**, **Transfers**, and **Returns** across **years**.        |
| 🧹 **Data Cleaning**        | - Handled **null values** and **outliers** <br> - Transformed and renamed columns |

---

## 📊 **Dataset Insights**  

- **Size**: 307,645 rows × 9 columns.  
- **Volume**: 21.1 MB.  
- **Key Metrics**:  
    - **Warehouse Sales** 📦: Major stock activity.  
    - **Retail Sales** 🛒: Customer purchase trends.  
    - **Returns** 🔄: Focus area to improve efficiency.  

---

## 🔍 **Data Cleaning Summary**  

### ✨ **Missing Values**  
- 🗂 `SUPPLIER` → Replaced with **"Default"**  
- 🏷 `ITEM TYPE` → Filled with **"NON-ALCOHOL"**  
-  `RETAIL SALES`, `RETAIL TRANSFERS` → Replaced with **0**
-  `ITEM CODE`→ **BC**,**WC**,**A** Replaced with **11**,**22**,balank 

### ✨ **Transformation**  
- Columns like `ITEM CODE` converted for **numerical clustering**.  
- 🏷️ New fields: **BRAND NAME**, **UNITS**, and **STD UNIT**.  

### ✨ **Correaltions of Numerical columns**
![Correaltions Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Before%20Opreation%20Heatmap.png)
The three scatter plots below all illustrate the relationship between Retail Transfers, Retail Sales, and Warehouse Sales for three different types of items.
 ![Correaltions Grap](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Before%20Treat%20outliears%20Retail%20Transfers%20VS%20Retail%20Sales.jpg)
In this first plot, the retail transfers have a very strong positive correlation with retail sales.
![Correaltions Grap](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Before%20Treat%20Outlier%20Warehouse_Sales%20VS%20Retail%20Sales.jpg)
The second plot reveals that the correlation between Warehouse Sales and Retail Sales has an evident group of higher warehouse sales occurring in tandem with a relatively moderate retail sale. 
![Correaltions Grap](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Before%20Treat%20Outlier%20Warehouse_Sales%20VS%20Retail%20Transfers.jpg)
The third plot, showing the relationship between Warehouse Sales and Retail Transfers has a positive trend such that Retail Transfers increase with growing Warehouse Sales. Linear trend lines in all plots highlight positive correlations among all variables.

### ✨ **Outliers**  
- Outliers identified in **Warehouse Sales** and **Retail Transfers**,**Retail Sales**.
  
![Outliers](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/checked%20outlier.jpg)
 
Visualization (checked_outlier.png): This barplot summary identifies features with potential outliers, thus helping to prioritize which attributes require treatment
---

## 📈 **Exploratory Data Analysis (EDA)**  
---

### 📊 **Major Insights**  

1. 🛒 **Retail Sales Insights**:  
   ![Retail Sales Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Retail%20Sales%20by%20Item%20Type.jpg)  
   - Wine and Beer : Wine represents 34.4% of sales, and Beer makes up 26.2%
   - Liquor : Liquor accounts for the largest portion of sales at 37.2% Liquor dominates.
   - Other categorie : The remaining categories (Dunnage, Kegs, Non-Alcohol, REF, and STR Supplies) each represent less than 1% of total sales, indicating they are not major contributors to overall revenue.
   ![Retail Sales Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Total%20Retail%20Sales%20by%20monthly.jpg) 
   - Total retail sales during the 7th month (July), reaching the highest value of 277,634.It shows seasonal or specfic events druing this moth  

---

2. 📦 **Warehouse Sales Insights**:  
   ![Warehouse Sales Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Warehouse%20Sales%20by%20Item%20Type.jpg)  
   - Beer : Beer constitutes a massive 82.4% of all dominates warehouse sales.
   - Wine : Wine represents 14.6% of sales, a significantly smaller portion compared to beer.
   - other categories: All other categories (Dunnage, Kegs, Liquor, Non-Alcohol, REF, and STR Supplies) each account for less than 1% of total sales, indicating they have a negligible impact on overall warehouse revenue.  

---

3. 🔄 **Returns Trends**:  
   ![Returns Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Return%20by%20years.jpg)
   - 2017: A significant 71.4% of all returns occurred in 2017 massive returns.
   - 2019: 2019 accounted for 21.4% of the returns had a moderate amount of returns.
   - 2018: Saw few returns Only 7.1% of returns happened in 2018.
   - 2020: The chart indicates 0.0% returns for 2020 No returns in.
   ![Return Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Transfers%20Return%20by%20years.jpg)  
   - 2017 : In 2017 saw the highest proportion of returns, significant 58.3% of transfer returns occurred.
   - 2019 : In 2019 had a notable share of returns making it the second-highest year for returns, accounted for 27.9% of the returns.
   - 2018 and 2020 : In 2018 represents 8.3% of returns , while 2020 has the smallest share at 5.4% had smaller proportions. 

---

4. 🚚 **Transfers Trends Insights**:  
   ![Transfers Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Retail%20Transfers%20by%20item%20type.jpg)
   - Liquor : It accounts for the largest portion of transfers at 37.3% to retail shops.
   - Wine and Beer : Wine represents 34.4% of transfers, while Beer makes up 26.5% are also frequently transferred in retail shops.
   - Other categories: The remaining categories (Dunnage, Kegs, Non-Alcohol, REF, and STR Supplies) each represent less than 1% of total transfers, indicating they are not frequently moved.
   ![Transfers Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Total%20Retail%20Transfers%20by%20monthly.jpg)
   - Peak Transfer Month: July 7 stands out with the highest number of transfers at 273,549, suggesting a significant event or seasonal factor driving increased activity during this period.
   - Consistent Activity: September 9 and November 11 also show notably high transfer numbers, indicating consistent activity throughout the year with potential spikes around certain periods.
   - Lowest Transfer Month: April 4 has the fewest transfers at 83,672, suggesting a potential lull in retail activity during this time.
---

5. 📊 **Yearly Comparison**:  
   ![Year Comparison Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Retail%20Transfers%20by%20years.jpg)
   - 2017: 31.7% had stock transfer to retail shops
   - 2018: In 2018 had transferred 7.2% stock to retail shops lowest.
   - 2019: 44.9% of stock transferred in 2019 largest stock delivaried 
   - 2020: 16.2% of stock stock were transferred in 2020 
   ![Reail Sales Graph](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Retails%20Sales%20by%20years.jpg)
   - 2019 : It had the largest share, making it the most successful year represented for 44.4% of total sales.
   - 2017 : 31.8% of sales occurred in 2017, making it the second-highest performing year.
   - 2020 : 16.7% of sales took place in 2020.
   - 2018 : Only 7.1% of sales were recorded in 2018.
   ![year comparison](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Warehouse%20Sales%20by%20years.jpg)
   - 2019 : has the largest share, accounting for 48.9% of total dispatches over the four years.
   - 2017 : 33.6%, indicating a significant portion of dispatches occurred that year.
   - 2020 : The accounts for 10.1%, less than half of the dispatches in 2017.
   - 2018 : It has the smallest share at 7.4%, showing the lowest dispatch activity among the four years.
   ![Warehouse Year Dispatch](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Warehouse%20dispatch%20Units%20by%20years.jpg)
   - 2017: 30.1% follow with 2019 it the second-highest performing year.
   - 2018: 6.7% had making sales in 2018.
   - 2019: 45.6% of warehouse sales had the largest sales.
   - 2020: In 2020 it only made 17.7% of sales across the warehouse.
   ![years of warehouse,retail,tranfer](https://github.com/Nikhi001/Warehouse-And-Retail-Sales/blob/main/Years_with_warehouse_sales_and_retail_transfers_and_Retail_sales.jpg)
   - Warehouse Sales (Blue Bars): It shows huge fluctuations. They are highest in 2019, followed by 2017, then 2020, and lowest in 2018.
   - Retail Transfers (Red Dotted Line with Markers): Also changing, not in the same way of warehouse sales. The transfers are highest in 2017 and 2019, lower in 2020, and lowest in 2018.
   - Retail Sales (Pink Bars): Follow the same trend as retail transfers. The highest is 2019 and 2017, lower in 2020, and lowest in 2018.
 

---

## 🤖 **Next Steps: Machine Learning**   

With all insights gathered, we are now ready to implement **machine learning models** to predict product clusters and optimize inventory.  

---

## 📌 **Target Audience**   
- 📊 **Business Managers**: Inventory & strategy decisions.  
- 🎯 **Marketing Teams**: Design campaigns.  
- 💻 **Data Analysts**: Insights and data tools.  
- 🏢 **Market Stakeholders**: Competitive growth strategies.  

---

## 🎉 **Conclusion**   

This project delivers actionable insights into sales trends, stock optimization, and clustering analysis. Ready to take this further? Let’s **dive into predictions** and transform operations with machine learning! 
