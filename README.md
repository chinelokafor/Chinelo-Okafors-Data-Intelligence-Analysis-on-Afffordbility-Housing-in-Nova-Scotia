# Housing Affordability: A Critical Analysis
*A decision intelligence study for understanding the dynamics in Housing availability*

*By: Chinelo Okafor*

## Executive Summary
Housing affordability is a growing concern in Nova Scotia with rising home prices, increasing rent burdens and challenging mortgage conditions creating barriers for many individuals and families seeking stable housing. This study utilizes modern data analysis tools including Python, Tableau and various statistical methods to explore housing affordability in Nova Scotia. The primary focus will be on factors such as home prices, rent-to-income ratios, vacancy rates and mortgage rates with the goal of providing actionable insights for policymakers, housing developers and stakeholders to address the housing affordability crisis.

[Read detailed background information here](https://github.com/chinelokafor/Term-Project/blob/main/Background.md)

## Key Performance Indicators (KPIs)

1. **Average House Prices** - 
Tracking average house prices within Nova Scotia helps assess market trends, affordability shifts and the impact of economic factors, guiding policymakers in making informed housing decisions.
  -	Target: Monitor annual price changes to identify affordability shifts.
  -	Measured quarterly based on regional data from Statistics Canada and other sources.
    
  
2. **Home Price-to-Income Ratio** -
Measures the affordability of residential properties by comparing the median home sale price to the median household income of buyers. A higher ratio indicates lower affordability, meaning homes are more expensive relative to income.
- Monitor changes in affordability trends over time (2020 vs. 2021).
- Compare affodability across different buyer groups (First-time vs. Not First-time, Immigrants vs. Non-immigrants).
-	Identify groups most affected by affordability constraints.

 
3. **Vacancy Rates** -
Analyzing vacancy rates provides insights into rental supply and demand, helping identify regions that require targeted housing development and policy interventions.
- Target: Identify areas with high vacancy rates that could benefit from increased rental development.
- Measured monthly through real estate transaction data.


4. **Home Ownership Rates** -
Tracking home ownership rates provides insights into housing accessibility, economic stability, and affordability trends, helping policymakers develop strategies to support sustainable homeownership.
- The interest rates impacting homeownership affordability, reflecting broader economic conditions.
- Target: Track changes annually to assess the impact of policies on homeownership growth.


5. **Housing Supply** -
Measuring annual housing supply against growing demand helps ensure adequate development, supporting strategic initiatives to meet the evolving needs of Nova Scotia’s residents.
-  The number of new housing units built annually, assessing the adequacy of the supply to meet growing demand.
- Action: Increase the rate of housing construction in high-demand areas.

# Analysis

![Average Housing Prices](Average_Housing_Prices.png)

![RentIncomeRatio](Homepricetoincomeratio.png)

![Vacancyrates](Vacancyrates.png)

![Homeowner](Homeowner.png)

![Housingsupply](Housingsupply.png)



## Analysis of the Causal Impact of Residential Average Price on Housing Affordability in Nova Scotia


### Introduction 
This analysis explores the relationship between key housing affordability metrics in Nova Scotia using the following key performance index (KPI): average housing prices, home price-to-income ratio, vacancy rates, home ownership rates and housing supply while focusing on the causal impact of residential average price on the price-to-income ratio. By examining causal relationships, correlation patterns and employing causal inference techniques, the study aims to identify how changes in residential prices affect housing affordability while controlling for factors like median house price, vacancy rate, and new housing units (housing Supply). The findings are intended to shed light on the dynamics of the housing market and provide insights for improving housing affordability.


### Correlation Matrix Heatmap
The matrix heatmap shows the relationships among residential average price and median house price where it shows a moderate negative correlation of -0.35, meaning when one price metric increases, the other tends to decrease slightly, possibly indicating differences between the median and average prices. It also highlights Price-to-Income Ratio is negatively correlated with Residential Average Price (-0.31) and strongly negatively correlated with Vacancy Rate (-0.55). This suggests that as housing prices increase, affordability decreases, and higher vacancy rates might indicate lower affordability or market supply issues.
•	Vacancy Rate is positively correlated with Housing Units (housing supply) (0.35), suggesting that areas with more housing supply may experience lower vacancy rates, aligning with expectations in more competitive housing markets.
•	Housing Units has a weak correlation with other factors like Price-to-Income Ratio (0.14) and Median House Price (-0.01), showing that the number of housing units does not have a strong direct relationship with these measures, despite the causal inference diagram indicating a potential effect on prices.

![matrixheatmap](matrixheatmap.png)


### Causal Graph
The causal relationships shows that new housing units (housing supply) affects residential average price, which in turn influences the median house price and the price-to-income ratio. Higher residential average prices tend to worsen affordability (higher Price-to-Income Ratio) as prices rise.

![causalgraph](causalgraph.png)


### Causal Inference & Confounders
•	Confounders like interest rates and inflation could bias the results, affecting both prices and affordability.
•	The correlation matrix suggests potential indirect relationships but confounders such as income levels or interest rates should be considered for clearer causal inference.


### Causal Estimand
The causal estimand models the effect of residential average price on the price-to-income ratio, controlling for median house price, vacancy rate, and new housing units (housing supply) using a backdoor criterion.


### Realized Estimand
The realized estimand is specified as a linear regression model:
Price-to-Income Ratio ~ Residential Average Price + Vacancy Rate (%) + New Housing Unit (housing supply) + Median House Price ($).
This indicates that residential average price is being assessed for its effect on price-to-income ratio, adjusting for other factors (confounders).


### Estimate of Causal Effect
The mean estimate of the causal effect is 4.47×10−64.47 \times 10^ {-6}4.47×10−6, which suggests that the causal effect of residential average price on price-to-income ratio is very small, possibly negligible given the scale of the effect. This result indicates that the residential average price may have a minimal impact on the price-to-income ratio, or that the data does not provide sufficient variation or observations to detect a stronger effect.


### Potential Causal Pathways
Vacancy rate affects price-to-income ratio through housing supply and residential average price.
Higher vacancy rates might reduce housing prices, improving affordability.


### Refutation Analysis
The refutation analysis of the causal effect of residential average price on the price-to-income ratio yielded a p-value of 0.40. This suggests that fluctuations in residential average price may not have a meaningful or detectable impact on housing affordability as measured by the price-to-income ratio. The results imply that other confounding factors such as interest rates and income levels, might play a more dominant role in shaping affordability trends. 


### Conclusion
This analysis suggests that while residential average price has a theoretical impact on the price-to-income ratio, the estimated causal effect is extremely small and statistically insignificant with a value of 4.47e-6. The weak correlations observed in the heatmap between residential average price and affordability measures further support this finding. Additionally, while causal pathways indicate that higher vacancy rates may reduce prices and improve affordability, confounding factors such as interest rates and income levels may influence both residential average price and the price-to-income ratio, potentially biasing the results.






