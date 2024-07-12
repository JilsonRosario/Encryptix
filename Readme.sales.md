# Sales Prediction Using Python: Comprehensive Analysis Report

## 1. Executive Summary

This report presents a detailed analysis of the relationship between advertising expenditure across different media channels (TV, Radio, and Newspaper) and resulting sales.
Using Python-based data analysis and machine learning techniques, we've developed a predictive model to estimate sales based on advertising spend.
The model demonstrates high accuracy, explaining approximately 90% of the variance in sales, with TV advertising showing the strongest correlation to sales outcomes.

## 2. Introduction

### 2.1 Objective
To analyze the impact of advertising spend on sales and develop a predictive model for future sales estimation.

### 2.2 Dataset Overview
The analysis utilizes a dataset containing 200 data points, each representing advertising expenditures on TV, Radio, and Newspaper, along with corresponding sales figures.

## 3. Methodology

### 3.1 Data Preprocessing
- Data source: "advertising.csv"
- Tools used: Python, Pandas, Seaborn, Matplotlib, Scikit-learn

### 3.2 Exploratory Data Analysis (EDA)
- Statistical analysis
- Correlation analysis
- Visualization techniques: Scatter plots, Heatmap

### 3.3 Model Development
- Algorithm: Linear Regression
- Feature selection: TV, Radio, Newspaper advertising spend
- Target variable: Sales
- Data split: 80% training, 20% testing

## 4. Data Analysis

### 4.1 Descriptive Statistics

| Metric    | TV          | Radio      | Newspaper  | Sales      |
|-----------|-------------|------------|------------|------------|
| Mean      | $147,042.50 | $23,264.00 | $30,554.00 | $15,130.50 |
| Std Dev   | $85,854.24  | $14,846.81 | $21,778.62 | $5,283.89  |
| Minimum   | $700.00     | $0.00      | $300.00    | $1,600.00  |
| Maximum   | $296,400.00 | $49,600.00 | $114,000.00| $27,000.00 |

### 4.2 Correlation Analysis

| Variable   | TV     | Radio  | Newspaper | Sales  |
|------------|--------|--------|-----------|--------|
| TV         | 1.000  | 0.055  | 0.057     | 0.901  |
| Radio      | 0.055  | 1.000  | 0.354     | 0.350  |
| Newspaper  | 0.057  | 0.354  | 1.000     | 0.158  |
| Sales      | 0.901  | 0.350  | 0.158     | 1.000  |

Key findings:
- TV advertising shows the strongest correlation with sales (0.901)
- Radio advertising has a moderate positive correlation (0.350)
- Newspaper advertising shows a weak positive correlation (0.158)

## 5. Model Performance

### 5.1 Model Metrics

| Metric | Training Set | Testing Set |
|--------|--------------|-------------|
| RMSE   | $1,635.89    | $1,705.21   |
| R²     | 0.900        | 0.906       |

### 5.2 Interpretation
- The model explains approximately 90% of the variance in sales.
- On average, predictions deviate from actual sales by $1,635.89 to $1,705.21.
- Similar performance on training and testing sets indicates good generalization.

## 6. Key Findings

### 6.1 Advertising Impact
1. TV Advertising: Strongest impact on sales. Each $1,000 increase in TV ad spend is associated with an approximate $901 increase in sales, ceteris paribus.
2. Radio Advertising: Moderate impact. Each $1,000 increase is associated with about $350 in additional sales.
3. Newspaper Advertising: Weakest impact. Each $1,000 increase is linked to only about $158 in additional sales.

### 6.2 Model Accuracy
- The model captures 90.6% of the factors influencing sales in the test dataset.
- About 9.4% of sales variance remains unexplained, suggesting other influential factors not included in the model.

### 6.3 Predictive Capability
Two sample predictions:
1. Input: TV=$150,000, Radio=$30,000, Newspaper=$20,000
   Predicted Sales: $16,005.61
2. Input: TV=$200,000, Radio=$40,000, Newspaper=$35,000
   Predicted Sales: $19,805.58

An increase of $50,000 in TV spend, along with increases in other channels, is associated with a predicted sales increase of $3,799.97.

## 7. Recommendations

1. Prioritize TV Advertising: Given its strong correlation with sales, allocate a larger portion of the advertising budget to TV.
2. Optimize Radio Advertising: Consider moderate increases in radio advertising budget, as it shows a positive impact on sales.
3. Reassess Newspaper Advertising: Given its weak correlation with sales, evaluate the effectiveness of current newspaper advertising strategies.
4. Utilize the Predictive Model: Use this model to estimate potential sales returns for different advertising budget allocations.
5. Continuous Monitoring: Regularly update the model with new data to maintain its accuracy and adapt to market changes.

## 8. Limitations and Future Work

### 8.1 Limitations
- The model assumes a linear relationship between advertising spend and sales.
- Other potential influencing factors (e.g., seasonality, economic conditions) are not considered.
- The dataset size (200 samples) may limit the model's generalizability to larger scales.

### 8.2 Future Work
- Incorporate additional variables that may influence sales.
- Explore non-linear modeling techniques to capture more complex relationships.
- Conduct time series analysis to account for temporal trends and seasonality.
- Expand the dataset to improve model robustness and generalizability.

## 9. Conclusion

This analysis provides valuable insights into the relationship between advertising expenditure and sales. The developed linear regression model demonstrates strong predictive power, explaining about 90% of the variance in sales. TV advertising emerges as the most influential factor, followed by radio, while newspaper advertising shows a weaker relationship. These findings can guide strategic decisions in advertising budget allocation to optimize sales performance.
