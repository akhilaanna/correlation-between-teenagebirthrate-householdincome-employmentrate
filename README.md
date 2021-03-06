# Association Between Teenage Birth Rate, Household Income, and Employment Rate in Baltimore City, Maryland 

## Background Information 
Baltimore City is a metropolitan area in Maryland known for its rich cultural history and diverse neighborhoods. Being a major city in the United States, there are key economic and social/health factors that should be reviewed frequently in order to assess its stablity and quality of living. Examples of economic factors that can define a city's stability are [employment rate](https://www.healthypeople.gov/subtopics-of-sdoh/economic-stability) and [household income](https://www.countyhealthrankings.org/explore-health-rankings/measures-data-sources/county-health-rankings-model/health-factors/social-and-economic-factors), whereas social factors include access to healthcare, health outcomes, etc. One specific health outcome that Baltimore City has [historically struggled with is teenage birth rate](https://cnsmaryland.org/2002/02/05/baltimore-ranks-worst-in-country-for-births-to-teens-unmarried-mothers/). I was curious to see the relationship between these factors, so in this data analysis, I assess the relationship between a social factor (teenage birth rate) and an economic factor (household income) on one of the city's overall economic factors: employment rate. 

## Business Question 
How do social and economic factors make an impact on Baltimore City's employment rate? 

## Data Question 
What is the association between teenage birth rate and employment rate using a simple linear regression model? What is the association between teenage birth rate, household income, and employment rate using a multiple linear regression model? 

Metrics used: teenage birth rate, household income, employment rate in Baltimore City, MD 
Data retrieved from: [Opportunity Atlas](https://www.opportunityatlas.org/). 

## Data Analysis Process 

**1) Simple Linear Regression: Relationship between Teenage Birth Rate and Employment Rate** 
	
*Slope*: -0.141178494 --> The negative slope indicates that as teenage birth rate increases, employment rate decreases. The absolute value of the slope is a very small number (less than 1), so the trendline is relatively flat. This means that as the teenage birth rate rises, the employment decreases only a little bit. 		

*Intercept*: 0.773863032 --> When the teenage birth rate is 0, the employment rate is 0.774. 					

*R-squared*: 0.071476839 --> 7.15% of the data can be explained by the linear regression line (trendline). This is very low. Based on the chart, it seems that it should be higher; however, the arithmetic shows that the R-squared value is very small, meaning that the trendline does not explain the data very well. 

*Standard Error*: 0.08476408 --> On average, the predicted value is 0.085 units away from the actual value. 						

Employment Rate = -0.1412(Teenage Birth Rate) + 0.7739					

Employment Rate for the average teenage birth rate (0.307) is predicted to be 0.73, or 73%. 

![image](simple-lin-regression-visualization.png) 

**2) Multiple Linear Regression: Relationship between Teenage Birth Rate, Household Income, and Employment Rate**

*R-squared*: 0.496771549 --> 49.7% of the data can be explained by the linear regression line (trendline). This is relatively high compared to the R-squared value from the simple linear regression conducted before. This means that the equation accurately explains almost half the data.  

*Standard Error*: 0.039538306 --> On average, the predicted value is 0.04 units away from the actual value. This is a low number, meaning that there is less difference between the predicted and actual values than if the standard error were higher. 

*Coefficients*:	3.08E-06 (household income), 0.009663745 (teenage birth rate) --> The coefficient for household income is extremely low (3.08E-06), but this doesn't necessarily mean that the effect of household income on employment rate is small. Since the household income values are large (in tens of thousands), the coefficient ends up being smaller to compensate for those large values. Though the value is small, it is still positive, meaning that there is a positive association between household income and employment rate (as income increases, employment rate by a little bit.) 

The coefficient for teenage birth rate is also low, but not as low as the coefficient for household income. Though low, it is positive, so in this model, as teenage birth rate increases, employment rate increases a little bit. This contrasts the results from the simple linear regression, so further research may be necessary to reach a consistent conclusion. 

*Significance F*: 1.00426E-51 --> Significance F is the probability that the household income and teenage birth rate don't actually make a meaningful contribution to predicting employment rate. The signifcance F for this model is very low, which means that the variables do matter and do correlate with employment rate. 

*P-values*: 1.82983E-12 (household income), 0.774784043 (teenage birth rate) --> P-values smaller than 0.05 indicate that the null hypothesis can be rejected. The null hypothesis is that there is no statistically significant impact of the independent variables on the dependent variable, so rejecting it would mean that there is an impact. The p-value of the household income is very small, meaning that the variable has significant effects. The p-value of the teenage birth rate, however, is larger than 0.05, so the variable does not have a statistically significant effect. The significance F value suggests that overall the variables do matter, but when considered individually, the data shows that the teenage birth rate cannot be concluded to have a significant impact on emplyoment rate.

## Business Answer 

Social factors and economic factors can both make an impact on employment rate. The data from the simple linear regression showed that teenage birth rate can make an impact, but did not show significant results in the multiple linear regression. Household income was only used for the multiple linear regression, and the results from it showed that it does have an impact. 

## Recommendations 

While teenage birth rate does have a statistically significant assocation with employment rate based on the simple linear regression, the multiple linear regression's results show that it does not. Thus, these recommendations will focus on household income, which did show a statistically significant association with employment rate in the multiple linear regression analysis. The positive association between household income and employment rate (as shown by the slope/coefficient of the relationship) suggests that higher income is associated with higher employment. There are many theories for why this may be, but focusing on just one for now can be effective rather than attempting to make improvements across all areas at once. According to the [National Conference of State Legislatures](https://www.ncsl.org/research/labor-and-employment/barriers-to-work-low-income-unemployed-and-dislocated-workers.aspx), one thing that holds back many low-income individuals from employment is the cost to even be eligible. To elaborate, many jobs require licensing on some level, which costs money; the licensing can include background checks, paperwork processing, and coursework that can all pose signficiant financial burdens for people with lower incomes. This suggests that people who can afford the licensing, those with higher incomes, would be more likely to be employed, which can explain the association showed by the data. The NCSL recommends that people with lower incomes are given waivers for the costs of licensing, so that they have the opportunity to work just like people with higher incomes. 

Baltimore City's goal should be to ensure proper economic stability through the means of employment, which, according to the data, has the potential to be reached through a focus on matters surrounding household income. Fixing the issue of licensing serving as a financial threat to those with lower income is a good start to using the data analysis to make systemic changes in the community and reach the desired economic stability. 

Ultimately, the models from this data analysis are only predictions, and the equations generated from them can only explain so much about the relationships between the variables. The R-squared value for the multiple linear regression was about 50%, which is significantly higher, but still is not 100% accurate in predicting employment rate values. 

*Note: All information regarding licensing and its impacts on low-income individuals and employment is from the National Conference of State Legislatures. The source is hyperlinked.* 

## Further Research 

For further research, I am interested in assessing other factors that affect employment rate, such as social policies regarding housing, education, and discrimination. It is such a broad variable with many aspects affecting it, so there is much to research from here on. 

## Sources (in order of appearance)

1. https://www.healthypeople.gov/subtopics-of-sdoh/economic-stability
2. https://www.countyhealthrankings.org/explore-health-rankings/measures-data-sources/county-health-rankings-model/health-factors/social-and-economic-factors
3. https://cnsmaryland.org/2002/02/05/baltimore-ranks-worst-in-country-for-births-to-teens-unmarried-mothers/
4. https://www.opportunityatlas.org/
5. https://www.ncsl.org/research/labor-and-employment/barriers-to-work-low-income-unemployed-and-dislocated-workers.aspx
