# E-Commerce Customer Spending Analysis

## Overview

This project analyzes customer spending patterns in an e-commerce platform using R and statistical modeling techniques. The analysis focuses on identifying key factors that influence annual customer spending.

## Dataset

The dataset contains the following variables:
- Time on Website (minutes)
- Time on App (minutes)
- Average Session Length (minutes)
- Length of Membership (years)
- Yearly Amount Spent (USD)

## Analysis Approach

### Exploratory Data Analysis
- Visualized relationships between engagement metrics and spending
- Examined distributions of key variables
- Analyzed pairwise correlations between all numerical variables

### Statistical Modeling

#### Primary Model: Linear Regression
- Simple linear regression predicting Yearly Amount Spent from Length of Membership
- Multiple linear regression incorporating all engagement metrics

#### Model Validation
- 80/20 train-test split
- Calculated performance metrics:
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Percentage Error (MAPE)
  - R-squared (R2)

## Key Findings

1. Membership duration is the strongest predictor of customer spending (β = $64.22 per year)
2. Time spent on mobile app shows stronger correlation with spending than website time
3. The multiple regression model explains 98% of spending variation (R2 = 0.98)
4. Model achieves $9.97 RMSE on test data

## Usage

To reproduce this analysis:

1. Install required packages:
```r
install.packages(c("ggplot2", "knitr", "scales"))
```

2. Run the Quarto document:
```bash
quarto render analysis.qmd
```

## Files

- `analysis.qmd`: Main analysis document
- `data/ecomdata.csv`: Dataset
- `_quarto.yml`: Configuration file

## Dependencies

- R (v4.0+)
- Quarto (v1.2+)
- R Packages:
  - ggplot2
  - knitr
  - scales
