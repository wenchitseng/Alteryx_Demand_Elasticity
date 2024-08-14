# Demand Elasticity Analysis
This case study leverages Alteryx to explore price elasticity of demand, income elasticity of demand, and the factors influencing sales dynamics, with a focus on the impact of real disposable personal income and pricing strategies.

# Introduction
#### Dataset:
- **Historical Sales Report:** This dataset includes price and monthly sales performance from 2006 to 2023, which, along with personal income data, will be used to explore price elasticity of demand, income elasticity of demand, and to identify any seasonality in historical sales performance.
<div align=center>
<img width="545" alt="image" src="https://github.com/user-attachments/assets/fd55db81-eccc-43bc-95b2-fa94d66787c6">
</div>    

- **Real Disposable Personal Income:** This dataset is from FRED where record the monthly Real Disposable Personal Income from 1965 to 2023.
<div align=center>
<img width="283" alt="image" src="https://github.com/user-attachments/assets/2443ea97-e2c2-4040-a6a7-26a49d09206f">
</div>  

- **2024 Pricing Strategiy:** This dataset includes the company's 2024 pricing strategy. We will later compare it with the results of time series forecasts based on historical sales data to assess the accuracy of our predictions.
<div align=center>
<img width="701" alt="image" src="https://github.com/user-attachments/assets/076f224c-c7b5-4be6-b36d-1cef8b537b46">
</div>

# ① Data Transformation    
Since the Historical Sales Report and Real Disposable Personal Income datasets are raw and uncleaned, we first need to use the Preparation Tool to transform the data into a structured format. Then, we'll use the Join Tool to combine the datasets by the date column.The cleaned dataset is shown below (displaying only the first 5 rows):
|Date| Price | Sales | Income |
|---|-----|----|----|
|2006-01-01| 18.65| 98| 31111|
|2006-02-01| 18.65 |70| 31208|
|2006-03-01| 18.65| 52| 31260|
|2006-04-01| 18.75| 66 |31363|
|2006-05-01| 14.06| 469| 31454|

