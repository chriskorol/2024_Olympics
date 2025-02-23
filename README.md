# 2024 Olympics, Medals ~ GDP

## Introduction

The Olympic Medals ~ GDP project examines the relationship between a nation's economic strength and its performance at the Olympic Games. By leveraging statistical and econometric techniques, this study investigates whether higher GDP values correlate with better Olympic outcomes and explores the predictive power of GDP on medal totals.

## Background

Wealthier nations often have more resources to invest in sports infrastructure, athlete training, and competitive programs, which can influence their success at the Olympics. However, while economic strength is an important factor, other elements such as cultural priorities, government policies, and historical contexts also play a role. This project revisits these ideas using robust statistical analysis to quantify the relationship between GDP and Olympic medal counts.

## Tools Used

#### Programming Environment:

R

#### Data Manipulation & Analysis:

Base R
Statistical & Econometric Methods:

#### t-Tests & p-Values:

To assess the significance of our findings.

#### Linear Regression:

To build a predictive model relating GDP to the total medal count.

#### Data Sources:

Public Kaggle dataset from Mohamed Yosef.

## Analysis

The key regression model examined in this study is:

```r
lm(formula = total ~ gdp, data = data)
```

## Regression Output Overview:

_Regression Equation:_
total = 4.94 + 0.000269 × gdp

#### Interpretation of Coefficients:

_Intercept (4.94):_
This value represents the estimated total when GDP is zero. Although the intercept has a p-value of 0.0739 (marginally significant at the 10% level), it serves as the baseline for our model.

_GDP (0.000269):_
The coefficient for GDP is positive and statistically significant (p-value = 0.000778), indicating that as GDP increases, the total (medal count) is expected to rise. For each unit increase in GDP (depending on the measurement scale), the predicted total increases by 0.000269.

#### Model Performance:

_R-squared:_
Approximately 12.1%, meaning that GDP explains about 12.1% of the variance in the total medal count. This modest R-squared value suggests that while GDP is a significant predictor, many other factors likely influence Olympic performance.
_F-statistic:_ 12.12 with a corresponding p-value of 0.000778, which confirms the overall model is statistically significant.

## A Graphic Model

![Visualization of linear regression between the number of Olympic medals and the GDP of countries](https://github.com/chriskorol/2024_Olympics/blob/main/000016.png)

## What I Learned

#### Statistical Significance:

The analysis shows that GDP is a statistically significant predictor of the total medal count, as evidenced by the low p-value for the GDP coefficient.

#### Model Limitations:

Despite the significance of GDP, the model’s low R-squared (12.1%) indicates that a large portion of the variability in Olympic medals remains unexplained. This suggests that additional variables (such as population, sports investment, and cultural factors) might improve the model.

#### Practical Implications:

The findings imply that while economic strength contributes to Olympic success, it is only one part of a multifaceted picture. Nations may achieve unexpected results due to strategic policies or other external factors not captured by GDP alone.

## Insights

#### Positive Association:

The positive coefficient for GDP confirms that higher economic output is associated with increased medal counts. However, the magnitude of the effect is relatively small, suggesting that GDP impacts medal outcomes incrementally.

#### Need for Broader Models:

Given that GDP accounts for only 12.1% of the variance, future research should incorporate additional predictors. Enhancing the model with factors such as population size, government spending on sports, or historical performance might provide a more comprehensive understanding.

#### Statistical Rigor:

The application of t-tests, p-value assessments, and linear regression in R underscores the importance of rigorous statistical analysis when drawing conclusions from real-world data.

## Conclusion:

The _Olympic Medals ~ GDP_ project provides evidence of a positive, statistically significant relationship between a nation's GDP and its Olympic medal count. However, the limited explanatory power of GDP alone highlights the need for a more nuanced approach, incorporating additional variables to fully understand the drivers of Olympic success. By using R and econometric techniques, this analysis offers valuable insights while also paving the way for further research into the multifaceted determinants of international sports performance.
