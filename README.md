# 📝 Demand Elasticity Analysis
This case study leverages Alteryx to explore price elasticity of demand, income elasticity of demand, and the factors influencing sales dynamics, with a focus on the impact of real disposable personal income and pricing strategies.
<div align=center>
<img width="1168" alt="image" src="https://github.com/user-attachments/assets/6b4becb3-ade5-49c3-98a3-98a6d8e1c276">
</div>  

# Introduction
#### Dataset:
- **Historical Sales Report:** This dataset includes price and monthly sales performance from 2006 to 2023, which, along with personal income data, will be used to explore price elasticity of demand, income elasticity of demand, and to identify any seasonality in historical sales performance.
<div align=center>
<img width="546" alt="image" src="https://github.com/user-attachments/assets/8c428a11-6b01-458b-8411-9af542301e59">
</div>    

  
- **Real Disposable Personal Income:** This dataset is from FRED and records the monthly Real Disposable Personal Income from 1965 to 2023.
<div align=center>
<img width="283" alt="image" src="https://github.com/user-attachments/assets/f576284e-d075-4c86-bc46-f757543acdfd">
</div>  

  
- **2024 Pricing Strategiy:** This dataset includes the company's 2024 pricing strategy. We will later compare it with the results of time series forecasts based on historical sales data to assess the accuracy of our predictions.
<div align=center>
<img width="704" alt="image" src="https://github.com/user-attachments/assets/444820a2-409c-49b7-bb6e-af74996a9eac">
</div>

  
# ① Data Transformation   
<div align=center>
<img width="652" alt="image" src="https://github.com/user-attachments/assets/207f4886-5425-4ea2-9b6e-0eecec97c3d2">
</div>  
Since the Historical Sales Report and Real Disposable Personal Income datasets are raw and uncleaned, we need to use the Preparation Tool and Developer Tool to transform the data into a structured format. Then, we use the Join Tool to combine the datasets by the date column. Note: We used an Inner Join, so the date column in the joined table begins from 2006-01-01.  

The workflow and cleaned dataset is shown below (displaying only the first 5 rows):     


<div align="center">  
  
|Date| Price | Sales | Income |  
|---|-----|----|----|
|2006-01-01| 18.65| 98| 31111|
|2006-02-01| 18.65 |70| 31208|
|2006-03-01| 18.65| 52| 31260|
|2006-04-01| 18.75| 66 |31363|
|2006-05-01| 14.06| 469| 31454|  

  
</div>  


# ② Demand Elasticity
<div align=center>  
<img width="650" alt="image" src="https://github.com/user-attachments/assets/1e2cf7f0-8502-44d8-9882-704ea382ef1c">  
</div>

  
<div align=center>
<img width="300" alt="image" src="https://github.com/user-attachments/assets/b28225df-cf81-4b40-8d38-05ce819b8b32">  
</div>  

🔍 Finding (1):  
A price elasticity of demand of -3.709 indicates that the demand for the product is highly elastic, meaning a 1% price increase leads to a 3.70% decrease in quantity demanded. This aligns with economic theory, as highly elastic products are usually non-essential or luxury goods where consumers can easily find substitutes or
forego the purchase.  

  
🔍 Finding (2):
An income elasticity of demand of 0.9974 indicates the product is a normal good, with a 1% income increase leading to a 0.9974% rise in quantity demanded. This aligns with economic theory, as normal goods see demand rise with income. Since the elasticity is less than 1, it suggests the product is a necessity rather than a
luxury.

  
🔍 Finding (3):
There is no obvious seasonality for this product, as there is a consistently significant relationship between the month and demand.

  
🖋️ Conclusion:  
This product is highly likely to be an **essential good**, such as tissue, eggs, bread, etc.

# ③ Price Prediction
<div align=center>  
<img width="643" alt="image" src="https://github.com/user-attachments/assets/c7eee91e-a3e5-41d2-83cb-ae8fcdca429b">
</div>

<div align=center>
<img width="400" alt="image" src="https://github.com/user-attachments/assets/67df4809-94ff-4104-b7b2-1068cca6cfa2">
</div> 


