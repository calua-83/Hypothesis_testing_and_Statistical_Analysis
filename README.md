# Hypothesis Testing And Statistical Analysis Report
## Overview

This project investigates sales data from the Adventure Works database to examine relationships between product prices and sales quantities, territory-specific sales performance, and potential seasonal sales trends. Using SQL for data extraction and Python for analysis, we tested multiple hypotheses to understand underlying patterns and to provide actionable insights.

## Research Questions and Hypotheses
## Hypothesis 1: Higher Product Prices Correlate with Lower Sales Quantities
Objective: To determine if higher product prices lead to a decrease in sales quantities.
#### Data Collection
Queried the Adventure Works database using SQLite to extract relevant product data, including product names, quantities sold, and prices.
#### Statistical Analysis
1. Calculated the average price per product and month by dividing total sales by quantity.
2. Created two key columns: AveragePrice and Quantity, which were used to compute correlation.
3. Used Python (Pandas) to calculate the correlation between average price and quantity.
#### Findings
- The calculated correlation coefficient was -0.35, suggesting a moderate inverse relationship between price and quantity.
- Interpretation: The negative correlation implies that as product prices increase, quantities sold tend to decrease, which aligns with economic demand theory.
-Note: Although the correlation is moderate, other factors (e.g., product quality, promotions, seasonality) may influence sales.

![](https://github.com/calua-83/Hypothesis_testing_and_Statistical_Analysis/blob/main/Correlationbetween%20_Averageprice_Quantity.png?raw=true)

## Hypothesis 2: Sales Performance Varies Significantly Across Different Territories

Objective: To identify if there are significant differences in sales performance across different territories.

#### Data Collection
Retrieved sales data across all territories.
#### Statistical Analysis
Conducted an ANOVA test (using scipy.stats.f_oneway) to compare average sales across territories.
#### Findings
- F-statistic: 26.37
- p-value: 1.39e-08
- Interpretation: A large F-statistic and a p-value below 0.05 indicate significant variability in sales performance between territories, suggesting that sales are impacted by territory-specific factors.
     
![](https://github.com/calua-83/Hypothesis_testing_and_Statistical_Analysis/blob/main/sales_discribution_by_territory.png?raw=true)
### Resons and recomadation
     There can be several reasons for significant differences in sales performance across territories. The reasons can vary based on external factors, internal strategies, or market conditions. Here are 
     some common factors that could contribute to the variation:
     
  ###  Hypothesis 3: Sales are higher for certain product categories due to seasonal trends.   
  #### Collect Dataset To Use
  After executing the query and categorizing sales data by season, we analyzed total sales and quantities across product categories.
  This initial grouping provides a snapshot of how each product category performs in different seasons.
  
  #### Perform Statistical Analysis
  The ANOVA test was used to determine if there are significant differences in sales between the four seasons (Winter, Spring, Summer, and Fall). This test compares the means of sales across the seasons 
  and checks for significant variation.
•	F-value: The F-statistic helps assess the variance between the groups (sales across seasons) versus the variance within the groups (sales within each season).
•	p-value: The p-value indicates whether the observed differences in sales across the seasons are statistically significant.

  #### Findings
  The result from the ANOVA test is as follows:
    •	P-Value = X.XX
    •	Significance Level (α) = 0.05
 If the p-value is less than 0.05 (α), we reject the null hypothesis and conclude that sales vary significantly across different seasons. If it is greater than 0.05, 
 we fail to reject the null hypothesis, meaning there is no significant difference in sales across seasons.
 
 In our case: P-Value  = (p-value: 0.9129111905702538)
 Sales are not significantly different across seasons, implying that there is no strong seasonal effect on sales across the product categories.
 
  ![](https://github.com/calua-83/Hypothesis_testing_and_Statistical_Analysis/blob/main/seasonal_trends.png?raw=true)
  ### Resons and recomadation
  Further investigation is recommended to understand the lack of significant seasonal impact. Factors such as year-round demand, promotions, or product- 
  specific trends could be contributing to these results.

    


