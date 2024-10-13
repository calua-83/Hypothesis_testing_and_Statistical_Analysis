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
   -  Even though a value of -0.35 shows a moderate inverse relationship,It’s not a very strong correlation (like -1, which would indicate a perfect inverse relationship),
      but it does still suggest that there is some tendency for sales quantities to decrease as prices rise.

