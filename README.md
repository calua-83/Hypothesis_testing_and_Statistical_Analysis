# Hypothesis Testing And Statistical Analysis Report
##  Research questions and the hypothesis to test.
### Hypothesis 1: Higher product prices correlate with lower sales quantities.

#### Collect Dataset To Use
     -To check if higher product prices correlate with lower sales quantities, we use the  SQLite to query the Adventure Works databese for relevant data and 
      then analyzed it using Python to calculate correlations.
#### Perform Statistical Analysis
    1.The Database was queried to retrieve product names, quantities sold, and prices.
    2.I Calculated the average price for each product and month, by dividing TotalSales by Quantity.
    3.I then prepared Data for Correlation: You will need two columns: AveragePrice and Quantity. These will be used to compute the correlation.
    4. We then use pandas to calculate the correlation between average price and quantity.
  
#### Findings
On our calculations we recieved A correlation value of -0.35 which indicates the following:
   - Since the correlation is negative, it means that as the price of the product increases, the quantity sold tends to decrease.This is consistent with the basic economic principle of demand, where higher 
     prices often lead to lower demand
   - Even though a value of -0.35 shows a moderate inverse relationship,It’s not a very strong correlation (like -1, which would indicate a perfect inverse relationship),
     but it does still suggest that there is some tendency for sales quantities to decrease as prices rise.
   - In practical terms, other factors may also be influencing the quantity sold (like product quality, promotions, seasonality, or brand loyalty), but price still has a noticeable impact on sales.

### Hypothesis 2: Sales performance varies significantly across different territories.

#### Collect Dataset To Use
  - To check this you need to retrieve data across all territories for proper analysis

#### Perform Statistical Analysis
Now that we have the data needed, we can check for significant differences in sales performance across different territories using ANOVA (Analysis of Variance).
  - This is a suitable method when comparing means across multiple groups (territories in this case).
  - We have used scipy.stats.f_oneway to conduct the ANOVA test.
    
#### Findings
    Results of the calculation: F-statistic: 26.36559808520165, p-value: 1.3877277105065728e-08
    -  F-statistic: Measures the ratio of the variance between the groups to the variance within the groups, a larger F-statistic means more 
       variability between territories compared to variability within them.
    -  p-value: This tells you the likelihood that the observed differences in sales performance are due to random chance. If the p-value is less than 0.05 (or a chosen significance level), 
       we can conclude in our case that sales performance varies significantly across territories.
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
  
  ### Resons and recomadation


    


