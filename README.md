# Demand Elasticity Analysis
This case study leverages Alteryx to explore price elasticity of demand, income elasticity of demand, and the factors influencing sales dynamics, with a focus on the impact of real disposable personal income and pricing strategies.

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
Since the Historical Sales Report and Real Disposable Personal Income datasets are raw and uncleaned, we need to use the Preparation Tool and Developer Tool to transform the data into a structured format. Then, we use the Join Tool to combine the datasets by the date column.  

Note: We used an Inner Join, so the date column in the joined table begins from 2006-01-01.  

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

