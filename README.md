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
     
## Hypothesis 3: Sales are Higher for Certain Product Categories Due to Seasonal Trends 
Objective: To determine if certain product categories exhibit seasonal sales trends.
#### Data Collection
Extracted and categorized sales data by season to analyze total sales and quantities across product categories.
#### Statistical Analysis
Used an ANOVA test to check for significant differences in sales across Winter, Spring, Summer, and Fall.
F-statistic: Compares variance between groups (sales across seasons) and within groups (sales within each season).
p-value: Indicates if seasonal sales differences are statistically significant.
#### Findings
p-value: 0.9129
Interpretation: A p-value greater than 0.05 implies that sales do not vary significantly across seasons, suggesting a lack of strong seasonal effects on sales.
   ![](https://github.com/calua-83/Hypothesis_testing_and_Statistical_Analysis/blob/main/seasonal_trends.png?raw=true)
## Conclusion and Recommendations
- **Price Sensitivity:** The inverse correlation between price and quantity suggests that pricing strategy plays a significant role in influencing sales volumes.
- **Territory-Specific Performance:** Significant differences in sales across territories may be due to regional preferences, purchasing power, or localized marketing efforts. Consider targeted strategies for underperforming regions.
- **Lack of Seasonal Impact:** Further investigation is recommended to explore why seasonal trends are not impacting sales. Year-round demand, promotions, or product-specific factors might be at play.
    


